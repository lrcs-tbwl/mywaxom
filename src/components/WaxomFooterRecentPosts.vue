<template>
    <div class="waxom-foot-recent-posts recent-foot-posts footer-item">
        <span class="recent-foot-posts-head footer-head">Recent Posts</span>
        <waxom-footer-recent-post v-for="(post, idx) in recentFooterPosts" :key="idx" :recentPost="post" :index="idx"/>
    </div>
</template>
<script>
import WaxomFooterRecentPost from './WaxomFooterRecentPost.vue';

export default {
  name: 'waxom-foot-recent-posts',
  components: {
      WaxomFooterRecentPost
  },
  data() {
      return{
          recentFooterPosts: {
              '1': {
                  txt: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit',
                  date: {
                      datecode: '2015-09-08',
                      datetxt: 'September 08, 2015'
                  }
              },
              '2': {
                  txt: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit',
                  date: {
                      datecode: '2015-09-08',
                      datetxt: 'September 08, 2015'
                  }
              },
              '3': {
                  txt: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit',
                  date: {
                      datecode: '2015-09-08',
                      datetxt: 'September 08, 2015'
                  }
              },
          }
      }
  }
}
</script>
