<template>
<div>
  <div v-show="tabIndex === 1" class="waxom-header-slider-slogan">
        <span class="slogan-intro">Unique and Modern Design</span>
        <span class="slogan-heading">Portfolio PSD Template</span>
        <span class="slogan-txt">Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum.</span>
        <button class="get-started">Get Started</button>
  </div>
  <div v-show="tabIndex == 2" class="waxom-header-slider-slogan">
        <span class="slogan-intro">Unique and Modern Design</span>
        <span class="slogan-heading">Portfolio PSD Template</span>
        <span class="slogan-txt">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et</span>
        <button class="get-started">Get Started</button>
  </div>
  <div v-show="tabIndex == 3" class="waxom-header-slider-slogan">
        <span class="slogan-intro">Unique and Modern Design</span>
        <span class="slogan-heading">Portfolio PSD Template</span>
        <span class="slogan-txt">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin vestibulum pharetra varius. Ut vel volutpat urna. Etiam sit amet dui.</span>
        <button class="get-started">Get Started</button>
  </div>
  <div v-show="tabIndex == 4" class="waxom-header-slider-slogan">
        <span class="slogan-intro">Unique and Modern Design</span>
        <span class="slogan-heading">Portfolio PSD Template</span>
        <span class="slogan-txt">In faucibus orci sed bibendum finibus. Etiam sed fermentum nisl. Vivamus vel egestas nibh, nec scelerisque metus. Donec dapibus metus.</span>
        <button class="get-started">Get Started</button>
  </div>
  <div v-show="tabIndex == 5" class="waxom-header-slider-slogan">
        <span class="slogan-intro">Unique and Modern Design</span>
        <span class="slogan-heading">Portfolio PSD Template</span>
        <span class="slogan-txt">Duis placerat euismod urna sed laoreet. Aliquam tristique nibh felis. Duis ornare maximus quam nec aliquam. Phasellus luctus, sapien a.</span>
        <button class="get-started">Get Started</button>
  </div>
</div>
</template>

<script>

export default {
  name: 'waxom-header-slider-slogan',
  props: {
      tabIndex: Number
  },
  data() {
      return{
      }
  }
}
</script>