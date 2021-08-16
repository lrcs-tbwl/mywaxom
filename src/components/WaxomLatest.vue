<template>
  <div class="waxom-latest latest-projects">
      <span class="latest-projects-heading">Our Latest Projects.</span>
        <p class="latest-projects-txt">Investigationes demonstraverunt lectores legere me lius quod ii legunt saepius. Claritas est etiam <br> processus dynamicus, qui sequitur mutationem consuetudium.</p>
        <waxom-latest-filter @set-post-tag="setPostTag" :tag="this.postTag" />
        <div class="waxom-latest-post-wrapper">
            <waxom-latest-post v-for="(post, postName) in filteredPosts" :key="postName" :latestPost="post"/>
        </div>
        <div class="breaker"></div>
        <button class="latest-projects-last-btn" v-show="Object.keys(this.filteredPosts).length < 6" @click="setPostTag('All')">load more</button>
  </div>
</template>

<script>
import WaxomLatestFilter from './WaxomLatestFilter.vue';
import WaxomLatestPost from './WaxomLatestPost.vue'

export default {
  name: 'waxom-latest',
  components: {
      WaxomLatestFilter,
      WaxomLatestPost
  },
  data() {
      return{
        postTag: 'All',
        latestPosts: {
            'post1': {
                  title: 'Claritas Etiam Processus',
                  img: 'item1.png',
                  tags: ['Photography', 'Nature']
              },
              'post2': {
                  title: 'Quam Nutamus Farum',
                  img: 'item2.png',
                  tags: ['Graphic Design', 'Mock-Up']
              },
              'post3': {
                  title: 'Usus Legentis Videntur',
                  img: 'item3.png',
                  tags: ['Photography', 'Holiday']
              },
              'post4': {
                title: 'Claritas Etiam Processus',
                img: 'item4.png',
                tags: ['Photography', 'Nature']
              },
              'post5': {
                  title: 'Quam Nutamus Farum',
                  img: 'item5.png',
                  tags: ['Graphic Design', 'Mock-Up']
              },
              'post6': {
                  title: 'Usus Legentis Videntur',
                  img: 'item6.png',
                  tags: ['Photography', 'Holiday']
              },
        },
          filteredPosts: {},
          filteredPostKeys: []
      }
  }, 
  methods: {
      setPostTag(tag) {
          this.postTag = tag
      },
      filterPosts(arg) {
          let postId = 0;        
          this.filteredPosts =  {};

          for (let post in this.latestPosts) {
              if (arg == 'All') { 
                Object.assign(this.filteredPosts, this.latestPosts)
                //console.log(Object.keys(this.filteredPosts).length);
                }

              let tagList = this.latestPosts[post].tags.filter(tag => tag == arg);

              if (tagList.includes(arg)) {
                  postId += 1;

                  this.filteredPosts[postId] = this.latestPosts[post]
                  //console.log(Object.keys(this.filteredPosts).length);
              }
          }
      }
  },
  computed: {
  },
  watch: {
      postTag(v) {
          this.filterPosts(v)
          //console.log('current post tag: ' + this.postTag);
      },
  },
    created() {
      return Object.assign(this.filteredPosts, this.latestPosts)
  }
}
</script>
