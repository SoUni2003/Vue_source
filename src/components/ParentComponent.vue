<script setup>
 import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';


 const nghi = 'Nam'
 const isLogin = ref(true)
 const classStudent = {
    age: '8',
    class: '9A'
 }
 const login = () =>{
    isLogin.value = !isLogin.value
 }   
</script>


<template>

<ChildComponent  :title="nghi" :ischecked="isLogin" :student="classStudent"></ChildComponent>
<button :class="!isLogin ? 'login' : 'logout'" @click="login">{{ isLogin ? 'Logout': 'Login' }}</button>
</template>

<style>
.login{
    background: rgb(3, 168, 133);
    color: black;
    border-radius: 5px;
}

.logout {
 background: red;
 border-radius: 5px;
 color: black;

}

</style>
