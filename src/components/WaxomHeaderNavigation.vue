<template>
  <div class="waxom-header-navigation">
    <waxom-header-logo />

      <waxom-header-menu />
  </div>
</template>

<script>

import WaxomHeaderLogo from './WaxomHeaderLogo.vue';
import WaxomHeaderMenu from './WaxomHeaderMenu.vue';

export default {
  name: 'waxom-header-navigation',
  props: {

  },
  components: {
    WaxomHeaderLogo,
    WaxomHeaderMenu
  }
}
</script>

<style scoped>
</style>