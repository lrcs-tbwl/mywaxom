<template>
  <div class="waxom-header-slider">
    <a class="slider slider-left" @click="backToTab" :class="{'disabled-left-slider': this.activatedTab == 1}" ></a>
    <div class="slogan">
      <waxom-header-slider-slogan :tabIndex="this.activatedTab" />
      <div class="slogan-pagination">
          <a class="slogan-pagination-item" v-for="(tab, key) in tabs" :class="{'picked-tab': this.activatedTab == tab}" :key='key' @click="changeTab(key, tab)" href="#"></a>
      </div>
    </div>
    <a class="slider slider-right" @click="forwardForTab" :class="{'disabled-right-slider': this.activatedTab == this.tabs}"></a>
  </div>
</template>

<script>
import WaxomHeaderSliderSlogan from './WaxomHeaderSliderSlogan.vue';

export default {
  name: 'waxom-header-slider',
  props: {

  },
  components: {
    WaxomHeaderSliderSlogan
  },
  data() {
    return{
      tabNumber: 1,
      tabs: 5,
      activatedTab: 1
    }
  },
  methods: {
    changeTab(key, tab) {
      this.activatedTab = tab;
      console.log('key: ' + key + 'tab: ' + tab + ' tabNum: ' + this.tabNumber + ' activated: ' + this.activatedTab);
    },
    forwardForTab() {
      if(this.activatedTab == this.tabs) {
        return this.activatedTab = 1;
      }
      this.activatedTab += 1;
    }, 
    backToTab() {
      if(this.activatedTab == 1) {
        return this.activatedTab = this.tabs;
      }
      this.activatedTab -= 1;
    }
  },
}
</script>