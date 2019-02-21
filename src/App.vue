<template>
  <div id="app">
    <Header></Header>
    <img alt="Vue logo" src="./assets/logo.png"> <br>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>
    <GoodBye mensagem="Esta é a minha mensagem"/>
    <GoodBye mensagem="Esta é a OUTRA mensagem" /> -->
    <AddTodo v-on:create-todo="addTodo"/>
    <TarefasComponent v-bind:TarefaLista="tarefas" v-on:del-item="deleteTodo" />   <!-- "lalala" é um props do componente e "tarefas" diz respeito ao "data" neste file-->
    <!-- {{tarefas[0].title}} -->
  </div>
</template>

<script>
import Header from './components/layout/header.vue';
import TarefasComponent from './components/TodosList.vue';
import AddTodo from './components/AddTodo.vue';

/* import HelloWorld from './components/HelloWorld.vue';
import GoodBye from './components/MyOwn.vue'; */

export default {
  name: 'app',
  components: {
    Header,
    AddTodo,
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
          completed: false
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
  },
  methods: {
    deleteTodo(id) {
      console.log('You clicked the X and deleted: '+ id);
      this.tarefas = this.tarefas.filter(tarefa => tarefa.id !== id);
    },
    addTodo(newTodo) {
      this.tarefas = [...this.tarefas, newTodo];
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

input[type="button"]:hover {
  background-color: rgb(53, 53, 53);
  color: whitesmoke;
}
</style>
