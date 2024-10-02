<template>
    <div>
    <h1>Bai2:</h1>
      <h3>Màu sắc</h3>
      <input type="color" v-model="selectedColor" />
      <div
        :style="{ width: '100px', height: '100px', backgroundColor: selectedColor, border: '1px solid black' }"
      ></div>
      <p>Mã màu: {{ selectedColor }}</p>
      <p>-------------------------------</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedColor: "#000000",
      };
    },
  };
  </script>
  
  <style scoped>
  </style>
  