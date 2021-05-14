<template>
<div :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{task.text}}
        <i @click="onDelete(task.id)" class="fas fa-trash"></i>
    </h3>
    <p>{{task.day}}</p>
</div>
    
</template>

<script>
    export default {
        name:'Task',
        props:{
            task: Object,
        },
        methods:{
            onDelete(id){
                this.$emit('delete-task', id)
            }
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