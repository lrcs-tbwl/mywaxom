<template>
    <div class="footer-widgets footer-item">
        <span class="footer-head">Dribble Widgets</span>
        <waxom-footer-widget v-for="(widget, idx) in footerDribbleWidgets" :key="idx" :index="idx" :widget="widget" />
    </div>
</template>
<script>
import WaxomFooterWidget from './WaxomFooterWidget.vue';

export default {
  name: 'waxom-footer-widgets',
  components: {
    WaxomFooterWidget
  },
  data() {
    return{
      footerDribbleWidgets: {
        '1': {
          src: 'widget_item1.png'
        },
        '2': {
          src: 'widget_item2.png'
        },
        '3': {
          src: 'widget_item3.png'
        },
        '4': {
          src: 'widget_item4.png'
        },
      }
    }
  }
}
</script>