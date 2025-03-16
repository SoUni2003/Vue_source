<script setup>
    defineProps({
        title: String,
        ischecked: Boolean,
    })
</script>

<template>
    <p>Title here 123: {{ title }}</p>
    <br>

    <h1 v-if="!ischecked">Login</h1>
    <h1 v-else>Welcome user {{ title }}</h1>
</template>

