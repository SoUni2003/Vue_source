<script setup>
 import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';


 const nghi = 'Nam'
 const isLogin = ref(true)
 const login = () =>{
    isLogin.value = !isLogin.value
 }   
</script>


<template>

<ChildComponent :title="nghi" :ischecked="isLogin"></ChildComponent>
<button @click="login">{{ isLogin ? 'Logout': 'Login' }}</button>
</template>
