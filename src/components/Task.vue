<template>
<div @dblclick="$emit('toggle-task', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{task.text}}
        <i @click="$emit('delete-task', task.id)" class="fas fa-trash"></i>
    </h3>
    <p>{{task.day}}</p>
</div>
    
</template>

<script>
    export default {
        name:'Task',
        props:{
            task: Object,
        }
    }
</script>

<style lang="css" scoped>
    .task{
        background-color: rgb(226, 226, 226);
        margin: 0.7rem;
        padding: 0.05rem 0.5rem;
        cursor:pointer;
    }
    .task.reminder{
        border-left: 0.4rem solid green;
    }
    .task h3{
        display:flex;
        align-items: center;
        justify-content: space-between;
    }
</style>