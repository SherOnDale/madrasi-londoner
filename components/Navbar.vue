<template>
  <div class="navbar__container">
    <div v-for="item in navbarItems" :key="item.name" class="navbar__item">
      <nuxt-link :to="item.route" class="navbar__link" v-html="svg[item.icon]"/>
    </div>
  </div>
</template>

<script>
import svg from '@/assets/svg.js'

export default {
  data() {
    return {
      navbarItems: [
        {
          name: 'home',
          route: '/',
          icon: 'person'
        },
        {
          name: 'contact',
          route: '/contact',
          icon: 'contact'
        }
      ],
      svg
    }
  }
}
</script>

<style>
.navbar__container {
  display: flex;
  flex-direction: column;
}
</style>
