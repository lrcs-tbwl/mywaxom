<template>
  <div class="waxom-recent-posts recent-posts">
      <span class="recent-posts-heading">Recent Posts.</span>
        <p class="recent-posts-descr">Investigationes demonstraverunt lectores legere me lius quod ii legunt saepius. Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.</p>
        <div class="breaker"></div>
        <waxom-recent-post v-for="(post, postName) in filteredRecentPosts" :key="postName" :recentPost="post" />
        <div class="breaker"></div>
        <div class="recent-posts-buttons">
            <button class="recent-posts-btn" @click="changePage('-')">
                <svg class="recent-posts-btn-svg" :class="{ 'recent-posts-btn-svg-disabled': this.page == 1}" width="22" height="22" viewBox="0 0 22 22" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.58 10.4298L12.35 5.65978C12.64 5.36978 13.11 5.36978 13.4 5.65978C13.68 5.94978 13.68 6.41978 13.4 6.69978L9.14 10.9598L13.4 15.2098C13.68 15.4998 13.68 15.9598 13.4 16.2498C13.11 16.5398 12.64 16.5398 12.35 16.2498L7.58 11.4798C7.44 11.3298 7.37 11.1498 7.37 10.9598C7.37 10.7698 7.44 10.5798 7.58 10.4298ZM10.99 0.0297852C17.05 0.0297852 21.97 4.93979 21.97 11.0098C21.97 17.0798 17.05 21.9898 10.99 21.9898C4.92 21.9898 0 17.0798 0 11.0098C0 4.93979 4.92 0.0297852 10.99 0.0297852ZM10.99 20.5198C16.23 20.5198 20.5 16.2498 20.5 11.0098C20.5 5.76979 16.23 1.49979 10.99 1.49979C5.74 1.49979 1.47 5.76979 1.47 11.0098C1.47 16.2498 5.74 20.5198 10.99 20.5198Z" />
                </svg>
            </button>
            <button class="recent-posts-btn" @click="changePage('+')" >
                <svg class="recent-posts-btn-svg" :class="{'recent-posts-btn-svg-disabled': this.page ==  this.pageLength}" width="22" height="22" viewBox="0 0 22 22" xmlns="http://www.w3.org/2000/svg">
                    <path d="M14.42 10.4298L9.64003 5.65978C9.36003 5.36978 8.89003 5.36978 8.60003 5.65978C8.32003 5.94978 8.32003 6.41978 8.60003 6.69978L12.86 10.9598L8.60003 15.2098C8.32003 15.4998 8.32003 15.9598 8.60003 16.2498C8.89003 16.5398 9.36003 16.5398 9.64003 16.2498L14.42 11.4798C14.56 11.3298 14.63 11.1498 14.63 10.9598C14.63 10.7698 14.56 10.5798 14.42 10.4298ZM11.01 0.0297852C4.95003 0.0297852 0.0300293 4.93979 0.0300293 11.0098C0.0300293 17.0798 4.95003 21.9898 11.01 21.9898C17.08 21.9898 22 17.0798 22 11.0098C22 4.93979 17.08 0.0297852 11.01 0.0297852ZM11.01 20.5198C5.77003 20.5198 1.50003 16.2498 1.50003 11.0098C1.50003 5.76979 5.77003 1.49979 11.01 1.49979C16.26 1.49979 20.52 5.76979 20.52 11.0098C20.52 16.2498 16.26 20.5198 11.01 20.5198Z" />
                </svg>                   
            </button>
        </div>
  </div>
</template>

<script>
import WaxomRecentPost from './WaxomRecentPost.vue';

export default {
  name: 'waxom-recent-posts',
  components: {
      WaxomRecentPost
  },
  data() {
      return{
          recentPosts: {
                'post1': {
                    title: 'Lorem ipsum dolor sit amet1',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item.png',
                    date: {
                        day: '30',
                        month: 'Sep.'
                        } 
                  },
                'post2': {
                    title: 'Lorem ipsum dolor sit amet2',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item2.png',
                    date: {
                        day: '30',
                        month: 'Sep.'
                  }
                },
                'post3': {
                    title: 'Lorem ipsum dolor sit amet3',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item3.png',
                    date: {
                        day: '30',
                        month: 'Sep.'
                  }
                },
                'post4': {
                    title: 'Lorem ipsum dolor sit amet4',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item.png',
                    date: {
                        day: '29',
                        month: 'Sep.'
                  }
                },
                'post5': {
                    title: 'Lorem ipsum dolor sit amet5',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item2.png',
                    date: {
                        day: '29',
                        month: 'Sep.'
                  }
                },
                'post6': {
                    title: 'Lorem ipsum dolor sit amet6',
                    txt: 'Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium.',
                    imgSrc: 'bg_item3.png',
                    date: {
                        day: '28',
                        month: 'Sep.'
                  }
                }
          },
          filteredRecentPosts: {},
          accessKeys: [],
          filteredAccessKeys: [],
          page: 1,
          pageLength: 0
      }
  },
  methods: {
      getPostKeys() {
          Object.keys(this.recentPosts).forEach((postKey) => {
          this.accessKeys.push(postKey)
      })
    },
    getCurrentKeys() {
        let start = (this.page - 1) * 3;
        let end = this.page * 3;
        this.filteredAccessKeys = this.accessKeys.slice(start, end);
    },
    filterRecentPosts() {
        let counterKey = 0;
        this.filteredRecentPosts = {}

        for (let post in this.recentPosts) {
            let currentPostKey = post;
            if (currentPostKey == this.filteredAccessKeys[counterKey]) { 
                this.filteredRecentPosts[currentPostKey] = this.recentPosts[post];
                counterKey += 1;
             }
        }
    },
    changePage(operation) {
          this.pageLength = this.accessKeys.length / 3;

          if (operation == '-') {
              if (this.page == 1) {
                  return;
              } else if (this.page > 1) {
                  return this.page -= 1;
              }
          } else if (operation == '+') {
              if (this.page == this.pageLength) {
                  return;
              } else if (this.page < this.pageLength) {
                  return this.page += 1;
              }
          }
      }
  },
  computed: {
  },
  created() {
      this.getPostKeys();
      this.getCurrentKeys();
      this.filterRecentPosts();
  },
  watch: {
      page() {
          this.getCurrentKeys();
          this.filterRecentPosts();
      }
  }
}
</script>
