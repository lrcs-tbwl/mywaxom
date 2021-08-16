<template>
 <div class="waxom-footer footer">
    <waxom-footer-upper />
    <waxom-footer-copyright />
 </div>
</template>

<script>
import WaxomFooterUpper from './WaxomFooterUpper.vue';

import WaxomFooterCopyright from './WaxomFooterCopyright.vue';

export default {
  name: 'waxom-footer',
  components: {
      WaxomFooterCopyright,
      WaxomFooterUpper
  }
}
</script>
