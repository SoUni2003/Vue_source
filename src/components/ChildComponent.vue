<!-- <script>
export default {
    props: {
        title: String,
        ischecked: Boolean,
        student: {
            age: Number,
            class: String,
        }
    }

};
</script> -->

<script setup lang="ts">
interface Student {
  age: number;
  class: string;
}

defineProps<{
  title: string;
  ischecked: boolean;
  student: Student;
}>();
</script>

<template>
  <p>Title here 123: {{ title }}</p>
  <br />

  <h2>Student Class: {{ student.class }}</h2>
  <h1 v-if="!ischecked">Login</h1>
  <h1 v-else>Welcome user {{ title }}</h1>

  <br />
</template>

<style>
p {
  color: red;
  font-size: 25px;
}
</style>
