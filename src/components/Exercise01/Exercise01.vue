<template>
  <form action="">
    <div>
        <h1>Bai1:</h1>
        Email: 
        <input v-model="username" type="text" placeholder="">
    </div>
    <h3>Gia tri: {{ username }}</h3>
    <p>-------------------------------</p>
  </form>
</template>

<script setup>
import {ref} from 'vue'

const username = ref({
    username:"",
})
</script>

<style>

</style>