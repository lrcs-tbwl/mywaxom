<template>
    <section class="waxom-footer-upper footer-upper">
        <waxom-footer-logo />
        <waxom-footer-recent-posts />
        <waxom-footer-twitter />
        <waxom-footer-widgets />
    </section>
</template>

<script>
import WaxomFooterLogo from './WaxomFooterLogo.vue';
import WaxomFooterRecentPosts from './WaxomFooterRecentPosts.vue';
import WaxomFooterTwitter from './WaxomFooterTwitter.vue';
import WaxomFooterWidgets from './WaxomFooterWidgets.vue';

export default {
  name: 'waxom-footer-upper',
  components: {
      WaxomFooterLogo,
      WaxomFooterRecentPosts,
      WaxomFooterTwitter,
      WaxomFooterWidgets
  }
}
</script>
