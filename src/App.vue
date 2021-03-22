<template>
  <div class="container">
      <Header title="Task Tracker"/>
      <Tasks :tasks="tasks" />
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
