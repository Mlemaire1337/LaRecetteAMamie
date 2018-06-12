<template>
  <div id="app">
    <HelloWorld/>
    <Msg/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Msg from './components/Msg'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Msg
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
