<template>
  <div class="container">
    <Header title="Task Tracker"/>
    <Tasks @delete-task="deleteTask" :tasks="tasks" />
  </div>
</template>

<script>
import Header from './components/Header'
import Tasks from './components/Tasks'

export default {
  name: 'App',
  components: {
    Header,
    Tasks
  },
  data() {
    return{
      tasks: []
    }
  },
  methods:{
    deleteTask(id){
      this.tasks= this.tasks.filter((task) => task.id !== id)
    }
  },
  created(){
      this.tasks= [
        {
          id:1,
          text: 'Doctors Appointment',
          day: 'March 1st at 2:30pm',
          reminder: true,
        },
        {
          id:2,
          text: 'Meeting',
          day: 'March 1st at 3:30pm',
          reminder: true,
        },
        {
          id:3,
          text: 'Yoga',
          day: 'March 3rd at 11:00am',
          reminder: false,
        },
      ]
  },
  
}
</script>

<style>
    * {
      font-family: cursive;
      font-weight: 400;
    }
    .container{
      border: 0.1rem solid black;
      margin: 4rem;
      padding: 1rem;
    }
</style>
