<template>
    <div class="goodbye">
        <p> {{mensagem}} </p>
        <p> {{mensagem}} </p>
        <p> {{mensagem}} </p>
    </div>
</template>

<script>
export default {
    name: 'GoodBye',
    props: {
        mensagem: String
    }

}
</script>

<style scoped>
    .goodbye {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        color: green;
        background-color: aquamarine;
    }
</style>
