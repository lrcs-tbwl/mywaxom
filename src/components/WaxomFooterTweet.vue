<template>
    <div class="waxom-foot-tweet footer-subitem" :class="{ 'underlined': index != '3'}" >
        <a href="#" class="footer-link">{{footerTweet.tweet}}</a>
        <time class="footer-datetime">{{ footerTweet.date }}</time>
    </div>
</template>
<script>

export default {
  name: 'waxom-foot-tweet',
  props: {
      footerTweet: Object,
      index: String
  }
}
</script>