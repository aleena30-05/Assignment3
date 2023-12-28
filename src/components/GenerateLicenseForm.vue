<template>
    <div class="form-container">
      <h2>Generate License</h2>
      <form @submit.prevent="generateLicense" class="license-form">
        <div class="form-group">
          <label for="productName">Product Name:</label>
          <select v-model="selectedProduct" id="productName" class="select-product">
            <option v-for="product in products" :value="product.name" :key="product.id">{{ product.name }}</option>
          </select>
        </div>
        <button type="submit" class="submit-btn">Generate License</button>
      </form>
    </div>
</template>

<script>
export default {
  // ...
}
</script>

<style scoped>
.form-container {
  max-width: 500px;
  margin: 20px auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h2 {
  text-align: center;
  color: #333;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
  color: #333;
}

.select-product {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  background-color: white;
  box-sizing: border-box;
}

.select-product:focus {
  outline: none;
  border-color: #42b983;
}

.submit-btn {
  width: 100%;
  padding: 10px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.submit-btn:hover {
  background-color: #369b7a;
}
</style>
