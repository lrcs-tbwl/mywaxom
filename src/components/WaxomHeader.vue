<template>
  <div class="waxom-header header">
    <waxom-header-navigation />
    <waxom-header-slider />
  </div>
</template>

<script>

import WaxomHeaderNavigation from './WaxomHeaderNavigation.vue';
import WaxomHeaderSlider from './WaxomHeaderSlider.vue';

export default {
  name: 'waxom-header',
  props: {

  },
  components: {
    WaxomHeaderNavigation,
    WaxomHeaderSlider
  }
}
</script>

<style scoped>
</style>
