<template>
    <div>
        <p>{{copyright}}</p>
    </div>
</template>

<script>
export default {
    data(){
        return{
            copyright: 'All right reserved, 2019 - 2020'
        }
    }
}
</script>

<style scoped>
div{
    margin-top: 250px;
}
p{
    color : black;
    background-color: yellow;
    padding: 20px;
    font-weight: bolder;
    font-size: 20px
}
</style>