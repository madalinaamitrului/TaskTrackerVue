<template>
  <h2>HTML Forms</h2>

  <form novalidate @click="addTask">
    <label for="task">Task</label>
    <input type="text" id="task" placeholder="Add task :)">
    <label for="dayAndTime">Task</label>
    <input type="text" id="dayAndTime" placeholder="Add day and time">
    <input type="checkbox" id="setReminder">
    <label for="setReminder">Set reminder</label>
  </form>
</template>

<script>
export default {
  name:'AddTask',
};
</script>

<style lang="css" scoped>
</style>