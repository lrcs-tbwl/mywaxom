<template>
        <div class="latest-projects-buttons waxom-latest-filter">
            <button class="latest-projects-btn" v-for="(tab, key) in tagTabs" :key="key" :class="{'lpp-btn-all': tab == 'All', 'latest-projects-btn-checked': this.activatedTab == tab}" @click="choosePostTag(tab)" >{{ tab }}</button>
        </div>
</template>
<script>

export default {
  name: 'waxom-latest-filter',
  props: {
      tag: String
  },
  emits: ['set-post-tag'],
  data() {
      return{
          tagTabs: ['All', 'Web Deisgn', 'Mobile App', 'Illustration', 'Photography' ],
          activatedTab: '',
      }
  },
  methods: {
      choosePostTag(tab) {
          this.activatedTab = tab;
          this.$emit("set-post-tag", tab)
      }
  },
  watch: {
      tag(n) {
          this.choosePostTag(n)
      }
  },
  mounted(){
      this.activatedTab = this.tag
  }
}
</script>