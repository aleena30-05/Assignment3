<template>
    <div class="table-container">
      <h2>Your Activated Licenses</h2>
      <table class="licenses-table">
        <thead>
          <tr>
            <th>License Key</th>
            <th>Product Name</th>
            <th>Activation Date</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="license in licenses" :key="license.id">
            <td>{{ license.key }}</td>
            <td>{{ license.productName }}</td>
            <td>{{ license.activationDate }}</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>

<script>
export default {
    data() {
      return {
        licenses: [
          { id: 1, key: 'XYZ123', productName: 'Product One', activationDate: '2023-01-01' },
          { id: 2, key: 'ABC456', productName: 'Product Two', activationDate: '2023-02-15' }
          // More licenses...
        ]
      };
    },
   
    name: 'UserLicenseView',
    props: {
      msg: String
    }
}
</script>

<style scoped>
.table-container {
  max-width: 100%;
  overflow-x: auto; /* Responsive design */
  margin: 20px 0;
}

.licenses-table {
  width: 100%;
  border-collapse: collapse;
  text-align: left;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.licenses-table th {
  background-color: #42b983;
  color: white;
  padding: 10px;
}

.licenses-table td {
  padding: 10px;
  border-bottom: 1px solid #ddd;
}

.licenses-table tr:nth-child(even) {
  background-color: #f9f9f9;
}
</style>
