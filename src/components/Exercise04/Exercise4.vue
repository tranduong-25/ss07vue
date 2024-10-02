<template>
    <div>
      <h1>Bai4:</h1>
      <h3>Tiến độ hoàn thành công việc:</h3>
      <input type="range" v-model="progress" min="0" max="100" step="1" />
      <p>Tiến độ: {{ progress }}%</p>
      <div 
        :style="{
          width: '100%', 
          height: '20px', 
          backgroundColor: '#f0f0f0',
          marginTop: '10px',
          border: '1px solid black'
        }">
        <div 
          :style="{
            width: progress + '%', 
            height: '100%', 
            backgroundColor: 'green'
          }">
        </div>
      </div>
      <p>-------------------------------</p>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  function useProgress() {
    const progress = ref(0);
  
    return { progress };
  }
  
  export function setup() {
    return useProgress();
  }
  </script>
  
  <style scoped>
  h3 {
    font-size: 18px;
    margin-bottom: 10px;
  }
  input[type="range"] {
    width: 100%;
    margin-bottom: 10px;
  }
  </style>
  