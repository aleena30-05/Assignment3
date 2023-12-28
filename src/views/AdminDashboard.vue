<template>
  <div class="AdminDashboard">
    <AddProductForm />
    <GenerateLicenseForm/>
    <LicenseList/>
  </div>
</template>

<script>
// @ is an alias to /src
import AddProductForm from '@/components/AddProductForm.vue';
import GenerateLicenseForm from '@/components/GenerateLicenseForm.vue';
import LicenseList from '@/components/LicenseList.vue'

export default {
  name: 'AdminView',
  components: {
    AddProductForm,
    GenerateLicenseForm,
    LicenseList,
  }
}
</script>
