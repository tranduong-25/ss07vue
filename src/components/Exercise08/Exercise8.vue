<template>
    <div>
      <h1>Bai8</h1>
      <h2>Form Đăng Ký</h2>
      <form @submit.prevent="register">
        <div>
          <label for="name">Tên:</label>
          <input type="text" v-model="user.name" id="name" />
        </div>
        
        <div>
          <label for="email">Email:</label>
          <input type="email" v-model="user.email" id="email" />
        </div>
  
        <div>
          <label for="password">Mật khẩu:</label>
          <input type="password" v-model="user.password" id="password" />
        </div>
  
        <div>
          <label for="confirmPassword">Nhập lại mật khẩu:</label>
          <input type="password" v-model="user.confirmPassword" id="confirmPassword" />
        </div>
  
        <button type="submit">Đăng ký</button>
      </form>
      <p>-------------------------------</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        user: {
          name: '',
          email: '',
          password: '',
          confirmPassword: ''
        }
      };
    },
    methods: {
      register() {
        console.log('Dữ liệu người dùng:', this.user);
      }
    }
  };
  </script>
  
  <style scoped>
    form {
      max-width: 400px;
      margin: 0 auto;
    }
    div {
      margin-bottom: 10px;
    }
    label {
      display: block;
      margin-bottom: 5px;
    }
    input {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
    }
    button {
      padding: 10px 20px;
      background-color: #007BFF;
      color: white;
      border: none;
      cursor: pointer;
    }
  </style>
  