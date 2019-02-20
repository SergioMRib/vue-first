<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png"> <br>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <GoodBye mensagem="Esta é a minha mensagem"/>
    <GoodBye mensagem="Esta é a OUTRA mensagem" /> -->
    <TarefasComponent v-bind:TarefaLista="tarefas"/>   <!-- "lalala" é um props do componente e "tarefas" diz respeito ao "data" neste file-->
    <!-- {{tarefas[0].title}} -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import GoodBye from './components/MyOwn.vue'
import TarefasComponent from './components/TodosList.vue'

export default {
  name: 'app',
  components: {
    TarefasComponent
    /* HelloWorld,
    GoodBye */
  },
  data() {
    return {
      tarefas: [
        {
          id:1,
          title: "Título PRIMEIRA",
          completed: true
        },
        {
          id:2,
          title: "Título SEGUNDA",
          completed: false
        },
        {
          id:3,
          title: "Título TERCEIRA",
          completed: false
        }
      ]
    }
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
