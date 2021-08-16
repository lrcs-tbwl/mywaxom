<template>
        <div class="latest-projects-project">
            <img width="370" height="237" :src="require(`@/assets/img/${latestPost.img}`)" alt="" class="latest-projects-img">
            <div class="latest-projects-project-descr">
                <span class="latest-projects-project-heading">{{ latestPost.title}}</span>
                <p class="latest-projects-project-txt"> {{latestPost.tags.join(', ')}}</p>
            </div>
        </div>
</template>
<script>

export default {
  name: 'waxom-latest-post',
  props: {
      latestPost: Object
  },
  data(){
      return{
      }
  }
}
</script>