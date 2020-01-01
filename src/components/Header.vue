<template>
    <div>
        <h1>Hello, This is {{msg}} </h1>
    </div>
</template>

<script>
export default {
    data(){
        return{
            msg: 'Todo from Vue'
        }
    }
}
</script>


<style scoped>
h1{
    color: yellow;
    background-color: black;
    padding: 10px;
}
</style>