<template>
  <div class="UserPage">
    <ActivateLicenseForm/>
    <UserLicenseView/>
  </div>
</template>

<script>
// @ is an alias to /src

import ActivateLicenseForm from '@/components/ActivateLicenseForm.vue';
import UserLicenseView from '@/components/UserLicenseList.vue'
export default {
  name: 'UserView',
  components: {
    
    ActivateLicenseForm,
    UserLicenseView
}
}
</script>
