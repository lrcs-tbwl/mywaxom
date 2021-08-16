<template>
    <img width="130" height="98" :src="require(`@/assets/img/${widget.src}`)" alt="" class="footer-widgets-img" :class="{ 'footer-widget-first': index == '1'}">

</template>
<script>

export default {
  name: 'waxom-footer-widget',
  props: {
      widget: Object,
      index: String
  }
}
</script>