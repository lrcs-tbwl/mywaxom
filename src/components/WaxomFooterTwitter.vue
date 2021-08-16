<template>
    <div class="waxom-foot-twitter our-twitter footer-item">
        <span class="footer-head">Our Twitter</span>
        <waxom-footer-tweet v-for="(tweet, idx) in footerTweets" :key="idx" :index="idx" :footerTweet="tweet" />
    </div>
</template>
<script>
import WaxomFooterTweet from './WaxomFooterTweet.vue';

export default {
  name: 'waxom-foot-twitter',
  components: {
      WaxomFooterTweet
  },
  data(){
      return{
          footerTweets: {
              '1': {
                  tweet: '@waxom Cum soluta nobis eleifend option congue nihil imperdiet doming',
                  date: '3 mins ago'
              },
              '2': {
                  tweet: 'Mirum est #envato notare quam littera gothica, quam nunc putamus parum anteposuerit litterarum',
                  date: '5 hours ago'
              },
              '3': {
                  tweet: 'Soluta nobis option bit.ly/1Hniso7',
                  date: '20 days ago'
              },
          }
      }
  }
}
</script>