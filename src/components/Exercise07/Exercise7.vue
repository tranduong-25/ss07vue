<template>
    <div>
      <h1>Bai7:</h1>
      <h3>Thêm mới sản phẩm</h3>
      <form @submit.prevent="addProduct">
        <div>
          <label for="productCode">Mã sản phẩm</label>
          <input type="text" id="productCode" v-model="productCode" />
        </div>
        <div>
          <label for="productName">Tên sản phẩm</label>
          <input type="text" id="productName" v-model="productName" />
        </div>
        <div>
          <label for="price">Giá</label>
          <input type="number" id="price" v-model.number="price" />
        </div>
        <div>
          <label for="quantity">Số lượng</label>
          <select id="quantity" v-model.number="quantity">
            <option v-for="n in 10" :key="n" :value="n">{{ n }}</option>
          </select>
        </div>
        <button type="submit">Thêm mới</button>
      </form>
  
      <div v-if="submitted">
        <h3>Sản phẩm đã thêm:</h3>
        <pre>{{ product }}</pre>
      </div>
      <p>-------------------------------</p>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        productCode: "",
        productName: "",
        price: 0,
        quantity: 1,
        submitted: false,
        product: {}
      };
    },
    methods: {
      addProduct() {
        this.product = {
          productCode: this.productCode,
          productName: this.productName,
          price: this.price,
          quantity: this.quantity
        };
        this.submitted = true;
        console.log(this.product); // Displays the product object in the console
      }
    }
  };
</script>
  
<style scoped>
  form div {
    margin-bottom: 10px;
  }
  
  button {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
  }
</style>
  