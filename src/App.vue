<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <qiantao></qiantao> -->
    <tentative></tentative>
    <zhiling></zhiling>
    <func></func>
    <DeepElementUI></DeepElementUI>
  </div>
</template>

<script>
import HelloWorld from './components/变量.vue'
import qiantao from './components/选择器.vue'
import zhiling from './components/指令.vue'
import func from './components/函数.vue'
import DeepElementUI from './components/DeepElementUI.vue'
import tentative from './components/尝试.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    qiantao,
    zhiling,
    func,
    DeepElementUI,
    tentative
  }
}
</script>

<style>
  .normalborder{
    border: 2px solid blue;
    margin: 10px;
    padding:10px;
  }

  .defualtmargin{
    margin: 10px;
  }
</style>
