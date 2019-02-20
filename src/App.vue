<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <GoodBye mensagem="Esta é a minha mensagem"/>
    <GoodBye mensagem="Esta é a OUTRA mensagem" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import GoodBye from './components/MyOwn.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    GoodBye
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
