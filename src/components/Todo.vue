<template>
    <div class="todo-item" v-bind:class="{'is-completed':item.completed}">
        <p>
            <input type="checkbox" v-on:change="toggleCompleted" v-bind:checked="item.completed">
            {{item.title}}
        </p>
    </div>
</template>

<script>
export default {
    props: ["item"],
    methods: {
        toggleCompleted() {
            this.item.completed = !this.item.completed;
        }
    }
}
</script>

<style scoped>
    .todo-item {
        background-color: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }
    .is-completed {
        text-decoration: line-through;
    }
</style>
