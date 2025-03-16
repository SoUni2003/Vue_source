<script setup>

import { ref } from 'vue';
import { count } from '../../store/CountStore.vue';



const checked = ref(false);

// const checkedF = () => {
//     checked!==checked
//     console.log(checked.value)
// }


const handleCLick = () =>{
    checked.value = !checked.value
}

console.log('checkm', checked.value)


</script>

<template>

<h1>This my count page</h1>
<p>Count now: {{ count }}</p>
<div class="inc_button">
    <button class="btn" @click="count++">Increas count</button>
    <span>++</span>
</div>

<br>
<button class="checked" @click="handleCLick">
    {{ checked ? 'need check' : 'checked' }}
</button>
<br>
<h1>THis my form</h1>

<p> Title here you need: {{ name }}</p>
<input type="text" v-model="name" placeholder="text me pls">

</template>

<style>

.checked{
    padding: 4px 4px;
    background: red;
}

.inc_button{
    position: relative;
}


span{
    position: absolute;
    justify-content: center;
    top: 0;
}
</style>