<template>
    <div>
      <h1>Bai5:</h1>
      <h3>Trước khi người dùng lựa chọn:</h3>
      <p>Giới tính:</p>
      <label>
        <input type="radio" v-model="gender" value="Nam" /> Nam
      </label>
      <label>
        <input type="radio" v-model="gender" value="Nữ" /> Nữ
      </label>
      <label>
        <input type="radio" v-model="gender" value="Khác" /> Khác
      </label>
  
      <h3>Sau khi người dùng lựa chọn:</h3>
      <p>Giới tính: {{ gender }}</p>
      <p>-------------------------------</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        gender: '',
      };
    },
  };
  </script>
  <style scoped>
  
  </style>