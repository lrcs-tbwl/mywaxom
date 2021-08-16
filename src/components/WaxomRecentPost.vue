<template>
<article class="waxom-recent-post recent-posts-article">
            <img width="370" height="220" :src="require(`@/assets/img/${recentPost.imgSrc}`)" alt="" class="recent-posts-img"/>
                <div class="recent-posts-datetime">
                    <span class="recent-posts-day">{{ recentPost.date.day }}</span>
                    <span class="recent-posts-month">{{ recentPost.date.month}} </span>
                </div>
            <div class="recent-posts-article-descr">
                <span class="recent-posts-article-heading">{{recentPost.title}} </span>
                <span class="recent-posts-article-txt">{{ recentPost.txt }}</span>
                <a href="#" class="recent-posts-article-link">Read More</a>
            </div>
        </article>
</template>

<script>

export default {
  name: 'waxom-recent-post',
  props: {
      recentPost: Object
  }
}
</script>