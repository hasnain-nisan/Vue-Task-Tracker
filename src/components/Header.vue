<template>
    <header>
        <div class="row px-4 mt-5 border-bottom-5 d-flex justify-content-between ">
                <h1>{{ title }}</h1>
                <Button color="green" text="Add Task" />
        </div>
        <hr class="mb-5">
    </header>
</template>

<script>
import Button from "./Button";
export default {
    name: 'Header',
    props: {
        title: String,
    },
    components: {
        Button,
    }
}
</script>