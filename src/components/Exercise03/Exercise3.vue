<template>
    <div>
      <h2>Bai3:</h2>
      <h3>Ngày sinh:</h3>
      <input type="date" v-model="birthDate" />
      <p v-if="birthDate">Ngày sinh: {{ birthDate }}</p>
      <p v-if="birthDate">{{ formattedDate }}</p>
      <p>--------------------------------</p>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue';
  
  function useDatePicker() {
    const birthDate = ref("");
    const formattedDate = computed(() => {
      if (!birthDate.value) return "";
      const date = new Date(birthDate.value);
      const day = String(date.getDate()).padStart(2, '0');
      const month = String(date.getMonth() + 1).padStart(2, '0'); 
      const year = date.getFullYear();
      return `${month}/${day}/${year}`;
    });
  
    return { birthDate, formattedDate };
  }
  
  export function setup() {
    return useDatePicker();
  }
  </script>
  
  <style scoped>
  
  </style>
  