<template>
  <div id="box">
    <toubu></toubu><!-- 顶部 -->
    <yuedu></yuedu><!-- 阅读记录 -->
    <tuijan></tuijan><!-- 推荐导航 -->
    <!-- <xiaoshuo></xiaoshuo>小说 -->
    <dibu></dibu><!-- 底部 -->
  </div>
</template>
<script>
import toubu from './components/toubu.vue'
import yuedu from './components/yuedu.vue'
import tuijan from './components/tuijan.vue'
// import xiaoshuo from './components/xiaoshuo.vue'
import dibu from './components/dibu.vue'
export default {
  components: {
    toubu,
    yuedu,
    tuijan,
    // xiaoshuo,
    dibu,
  },

}
</script>
<style scoped>
#box {
  width: 100%;
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
}
</style>
<style>
* {
  margin: 0;
  padding: 0;
}
</style>



