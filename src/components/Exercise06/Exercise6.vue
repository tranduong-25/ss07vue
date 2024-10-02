<template>
    <div>
      <h1>Bai6:</h1>
      <h3>Trước khi người dùng lựa chọn:</h3>
      <p>Sở thích:</p>
      <label>
        <input type="checkbox" v-model="hobbies" value="Đá bóng" /> Đá bóng
      </label>
      <label>
        <input type="checkbox" v-model="hobbies" value="Bóng chuyền" /> Bóng chuyền
      </label>
      <label>
        <input type="checkbox" v-model="hobbies" value="Code" /> Code
      </label>
      <label>
        <input type="checkbox" v-model="hobbies" value="Bơi lội" /> Bơi lội
      </label>
  
      <h3>Sau khi người dùng lựa chọn:</h3>
      <p>Sở thích: {{ hobbies }}</p>
      <p>-------------------------------</p>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        hobbies: [],
      };
    },
  };
</script>
<style>
</style>