<template>
  <div class="waxom-counters counters">
      <waxom-counter />
  </div>
</template>

<script>
import WaxomCounter from './WaxomCounter.vue';

export default {
  name: 'waxom-counters',
  components: {
    WaxomCounter
  }
  
  }
</script>
