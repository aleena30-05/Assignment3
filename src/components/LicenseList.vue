<template>
    <div class="table-container">
      <h2>Generated Licenses</h2>
      <table class="licenses-table">
        <thead>
          <tr>
            <th>License Key</th>
            <th>Product Name</th>
            <th>Generated Date</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="license in licenses" :key="license.key">
            <td>{{ license.key }}</td>
            <td>{{ license.productName }}</td>
            <td>{{ license.generatedDate }}</td>
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
          { key: 'ABC123', productName: 'Product One', generatedDate: '2023-01-01' },
          { key: 'XYZ456', productName: 'Product Two', generatedDate: '2023-02-15' }
          // Add other licenses here
        ]
      };
    },
    name: 'LicenseList',
    props: {
      msg: String
    }
}
</script>

<style scoped>
.table-container {
  max-width: 100%;
  overflow-x: auto; /* For responsive design */
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
