<template>
    <div >
        <div v-bind:key="tarefaEspecífica.id"  v-for="tarefaEspecífica in TarefaLista">
            <!-- <h3>{{tarefaEspecífica.title}}</h3> -->
            <todoItem v-bind:item="tarefaEspecífica" v-on:del-item="$emit('del-item', tarefaEspecífica.id)"/>
        </div>
    </div>
</template>

<script>
import todoItem from "./Todo.vue"

export default {
    /* name: "Tarefas", */
    components: {
        todoItem
    },
    props: ["TarefaLista"]

}
</script>

<style scoped>

</style>
