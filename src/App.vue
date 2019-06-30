<template>
  <div id="app">
    <HelloWorld msg="Welcome"/>
    <Sample01></Sample01>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Sample01 from "@/components/Sample01";

export default {
  name: 'app',
  components: {
    HelloWorld,
    Sample01
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
