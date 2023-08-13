<template>
  <div id="app">
    <top></top>
    <biaoqian></biaoqian>
    <yingyong></yingyong>
  </div>
</template>

<script>
import top from './components/top.vue'
import biaoqian from './components/biaoqian.vue'
import yingyong from './components/yingyong.vue'

export default {
  name: 'App',
  components: {
    top,
    biaoqian,
    yingyong,
  }
}
</script>
<style scoped>
#app{
width: 100%;
height: 100vh;
background: rgb(255, 255, 255);
}
</style>

<style>
*{
  margin: 0;
  padding: 0;
}
</style>

