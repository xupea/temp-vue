<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/背景+标题@2x.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style lang="less" scoped>
.home {
  img {
    width: 100%;
  }
}
</style>
