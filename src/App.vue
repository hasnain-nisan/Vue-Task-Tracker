<template>
  <div class="container">
      <Header title="Task Tracker"/>
      <Tasks @delete-task="deleteTask" :tasks="tasks" />
  </div>
</template>

<script>

import Header from './components/Header';
import Tasks from './components/Tasks';
export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data() {
    return {
      tasks: [],
    }
  },
  methods: {
    deleteTask(id) {
      if(confirm('Are you sure???')) {
        this.tasks = this.tasks.filter((task) => task.id !== id)
      }
    },
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Office Meeting',
        day: 'March 1st at 10:00 am',
        reminder: true,
      },
      {
        id: 2,
        text: 'Doctor appointment',
        day: 'March 1st at 12:00 pm',
        reminder: true,
      },
      {
        id: 3,
        text: 'Shopping',
        day: 'March 1st at 1:30 pm',
        reminder: false,
      },
    ]
  }
}
</script>

<style>

</style>
