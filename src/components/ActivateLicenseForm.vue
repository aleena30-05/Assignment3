<template>
    <div class="form-container">
      <h2>Activate License</h2>
      <form @submit.prevent="activateLicense" class="license-form">
        <div class="form-group">
          <input type="text" v-model="licenseKey" placeholder="License Key" class="input-field" />
        </div>
        <button type="submit" class="submit-btn">Activate</button>
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
  max-width: 400px;
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

.license-form {
  display: flex;
  flex-direction: column;
  gap: 10px; /* Spacing between form elements */
}

.input-field {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

.input-field:focus {
  outline: none;
  border-color: #42b983;
}

.submit-btn {
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
