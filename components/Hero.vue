<template>
  <div class="hero__container">
    <div class="hero__social">
      <div v-for="link in socialMedia" :key="link.icon">
        <a :href="link.url" target="_blank" rel="noopener noreferrer" v-html="svg[link.icon]"/>
      </div>
    </div>
    <div class="hero__title">
      I'm
      <span class="name">Joel Jasper</span>
    </div>
    <div class="hero__subtitle">A Passionate Digital Entrepreneur</div>
  </div>
</template>

<script>
import svg from '@/assets/svg.js'

export default {
  data() {
    return {
      svg,
      socialMedia: [
        {
          icon: 'instagram',
          url: 'https://instagram.com/iamjoel1996'
        },
        {
          icon: 'facebook',
          url: 'https://www.facebook.com/madrasi.londoner'
        },
        {
          icon: 'twitter',
          url: 'https://twitter.com/LondonerMadrasi'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.hero {
  &__social {
    display: flex;

    svg {
      height: 1rem;
      width: 1rem;
    }
  }
}
</style>
