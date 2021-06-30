<template>
  <div id="app">
    <div class="header">
      <img alt="yFiles logo" src="./assets/yfiles-logo.svg" />
      <h1>A Basic yFiles Integration in Vue.js</h1>
    </div>
    <graph-component></graph-component>
  </div>
</template>

<script>
import GraphComponent from './components/GraphComponent.vue'

export default {
  name: 'app',
  components: {
    GraphComponent,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.header {
  width: 100%;
  text-align: center;
}
.header img {
  height: 100px;
}
</style>
