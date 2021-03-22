<template>
    <button @click="onClick()" :style="{ background: color }" class="btn m-1">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        onClick() {
            alert('Button is clicked!!!')
        },
    }
}
</script>