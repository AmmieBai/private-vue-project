<template>
  <!-- 这里就是vue的视图层----即 MVVM 中的 V -->
  <div id="app">
    <h1>{{ msg }}</h1>
    <marquee></marquee>
  </div>
</template>
<script>
// import Vue from './vue'
import marquee from './components/marquee'
//  new出来的 vm 对象就是MVVM 中的 vm 调度者
  export default {
    name: 'app',
    //data 是vue的页面的数据层-----即 M，专门保存每个页面数据
    data() {
      return {
        msg: '这是一个vue 的数据'
      }
    }, 
    components: {
      marquee
    }
  }
</script>

<style>

</style>
