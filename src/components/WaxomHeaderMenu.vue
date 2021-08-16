<template>
    <nav class="menu waxom-header-menu">
        <div class="menu-list">
            <a v-for="(link, key) in menuItems" :key='key' :href="link" class="menu-list-item menu-link"> {{ key }}</a>
        </div>
        <a href="#" class="basket-mini">
                    <svg class="basket-mini-cart" width="18" height="24" viewBox="0 0 18 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M15 3H13.5C13.5 1.34 11.48 0 9 0C6.51 0 4.5 1.34 4.5 3H3C1.35 3 0 4.34 0 6V21C0 22.65 1.35 23.99 3 23.99H15C16.65 23.99 17.99 22.65 17.99 21V6C17.99 4.34 16.65 3 15 3ZM9 1.5C10.66 1.5 12 1.96 12 3H6C6 1.96 7.34 1.5 9 1.5ZM16.49 21C16.49 21.82 15.82 22.49 15 22.49H3C2.17 22.49 1.5 21.82 1.5 21V19.5H16.49V21ZM16.49 18H1.5V6C1.5 5.17 2.17 4.5 3 4.5H4.5V9H6V4.5H12V9H13.5V4.5H15C15.82 4.5 16.49 5.17 16.49 6V18Z"/>
                        </svg>
                        
        </a>
        <form action="#" method="post" class="search-mini">
                    <input type="search" class="search-mini-input">
                    <svg class="search-mini-icon" width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M23.76 22.68L17.57 16.59C19.19 14.82 20.19 12.49 20.19 9.93C20.19 4.44 15.67 0 10.09 0C4.52 0 0 4.44 0 9.93C0 15.42 4.52 19.86 10.09 19.86C12.5 19.86 14.71 19.03 16.45 17.64L22.66 23.76C22.97 24.06 23.46 24.06 23.76 23.76C24.06 23.46 24.06 22.98 23.76 22.68ZM10.09 18.33C5.38 18.33 1.55 14.57 1.55 9.93C1.55 5.29 5.38 1.52 10.09 1.52C14.81 1.52 18.63 5.29 18.63 9.93C18.63 14.57 14.81 18.33 10.09 18.33Z"/>
                        </svg>
        </form>
    </nav>
</template>

<script>
export default {
  name: 'waxom-header-menu',
  props: {

  },
  data() {
      return{
          menuItems: {
                  'Home' : '#',
                  'About Us' : '#',
                  'Portfolio' : '#',
                  'Features' : '#',
                  'Blog' : '#',
                  'Pricing' : '#',
                  'Shortcodes' : '#',
                  'Contact' : '#',
          }
      }
  }
}
</script>

<style scoped>
</style>