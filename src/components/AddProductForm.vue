<template>
    <div class="form-container">
      <h2>Add New Product</h2>
      <form @submit.prevent="addProduct" class="product-form">
        <div class="form-group">
          <label for="productName">Product Name:</label>
          <input type="text" id="productName" v-model="productName" placeholder="Enter product name" />
        </div>

        <div class="form-group">
          <label for="productVersion">Version:</label>
          <input type="text" id="productVersion" v-model="productVersion" placeholder="Enter version" />
        </div>

        <div class="form-group">
          <label for="description">Description:</label>
          <textarea id="description" v-model="description" placeholder="Enter description"></textarea>
        </div>

        <button type="submit" class="submit-btn">Add Product</button>
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
  margin: 0 auto;
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
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
  color: #333;
}

input[type="text"],
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type="text"]:focus,
textarea:focus {
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
  transition: background-color 0.3s ease;
}

.submit-btn:hover {
  background-color: #369b7a;
}
</style>
