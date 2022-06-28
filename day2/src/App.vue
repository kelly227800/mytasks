<template>
<!-- 目标: 点击按钮 - 把文字取反显示 - 再点击取反显示(回来了) -->
  <div>
    <h1>{{msg}}</h1>
    <button @click="reverse">逆转世界</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      msg: 'Hello, World',
    }
  },
  methods: {
    reverse() {
      this.msg = this.msg.split('').reverse().join('')
    }
  },
}
</script>

<style>

</style>
