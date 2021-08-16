<template>
    <div class="recent-foot-posts-item footer-subitem" :class="{ 'underlined': index != '3'}">
        <time class="recent-foot-posts-datetime footer-datetime" :datetime="recentPost.date.datecode">{{ recentPost.date.datetxt}}</time>
        <a href="#" class="recent-foot-posts-link footer-link">{{  recentPost.txt }}</a>
    </div>
</template>
<script>

export default {
  name: 'waxom-foot-recent-post',
  props: {
      recentPost: Object,
      index: String
  },
  data() {
      return{
      }
  }
}
</script>