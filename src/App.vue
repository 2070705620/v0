<template>
    <h1>Vue3</h1>
    <p>{{ msg }}</p>
    <button @click="changeMsg">Change Msg</button>
</template>
<script>
//vue3
import { ref, defineComponent } from 'vue'
export default defineComponent({
  setup() {
    const msg = ref('Hello Vue3')
    const changeMsg = () => {
      msg.value = 'Hello Vue3.1' + new Date().getTime()
    }
    return {
      msg,
      changeMsg
    }
  }
})
</script>