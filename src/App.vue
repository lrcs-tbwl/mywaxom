<template>
  <waxom-header />

  <waxom-services />
  
  <waxom-realization />

  <waxom-purchase />

  <waxom-latest /> 

  <waxom-video-presentation />

  <waxom-mobile-app />

  <waxom-counters />

  <waxom-recent-posts /> 

  <waxom-partners />

  <waxom-footer /> 
</template>

<script>
import WaxomHeader from './components/WaxomHeader.vue';
import WaxomServices from './components/WaxomServices.vue';
import WaxomRealization from './components/WaxomRealization.vue';
import WaxomPurchase from './components/WaxomPurchase.vue';
import WaxomLatest from './components/WaxomLatest.vue';
import WaxomVideoPresentation from './components/WaxomVideoPresentation.vue';
import WaxomMobileApp from './components/WaxomMobileApp.vue';
import WaxomCounters from './components/WaxomCounters.vue';
import WaxomRecentPosts from './components/WaxomRecentPosts.vue';
import WaxomPartners from './components/WaxomPartners.vue';
import WaxomFooter from './components/WaxomFooter.vue';
 
export default {
  name: 'App',
  components: {
    WaxomHeader,
    WaxomServices,
    WaxomRealization,
    WaxomPurchase,
    WaxomLatest,
    WaxomVideoPresentation,
    WaxomMobileApp,
    WaxomCounters,
    WaxomRecentPosts,
    WaxomPartners,
    WaxomFooter
  }
}
</script>

<style>
</style>
