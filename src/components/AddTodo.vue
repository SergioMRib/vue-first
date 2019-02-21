<template>
    <div>
        <form v-on:submit="createTodo">
            <input type="text" v-model="title" name="title"  placeholder="Add todo...">
            <input type="submit" value="submit" class="btn">
        </form>
    </div>
</template>

<script>
import uuid from 'uuid'
export default {
    data() {
        return {
            title: ''  //this is needed to link v-model="title" to a data; The other data will be created on the method
        }
    },
    methods: {
        createTodo(event) {
            event.preventDefault();
            const newTodo = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            };
            // Send up to parent
            this.$emit('create-todo', newTodo);

            //erase the form text
            this.title = '';
        }
    }
}
</script>

<style scoped>
    form {
        display: grid;
        grid-template-columns: 4fr 1fr;
    }
</style>
