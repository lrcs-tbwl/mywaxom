<template>
  <div class="waxom-services services">
      <waxom-service />
  </div>
</template>

<script>

import WaxomService from './WaxomService.vue';


export default {
  name: 'waxom-services',
  props: {

  },
  components: {
      WaxomService
  }
}
</script>

<style scoped>
</style>