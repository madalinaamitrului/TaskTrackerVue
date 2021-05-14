<template>
    <button @click="onClick()" :style="{background: color, border: color}">{{ text }}</button>
</template>

<script>
    export default {
        name: 'Button',
        props:{
            text: String,
            color: String,
        },
        methods: {
            onClick(){
                
            }
        }
    }
</script>

<style lang="css" scoped>
    button{ 
        padding:0.5rem;
        color: white;
        border-radius: 5px;
    }
</style>