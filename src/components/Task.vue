<template>
    <div :class="[task.reminder ? 'border-left border-success' : '', 'row d-flex justify-content-between bg-light m-2']">
        <div class="p-2">
            <h3>{{ task.text }}</h3>
            <p>{{ task.day }}</p>
        </div>
        <div class="justify-content-center">
            <i @click="deleteTask(task.id)" class="btn btn-danger fas fa-backspace"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object,
    },
    methods: {
        deleteTask(task) {
            console.log(task)
        }
    }
}
</script>

<style scoped>
 .border-success {
     border-radius: 5px;
     border-width: 5px !important;
 }
</style>