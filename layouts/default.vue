<template>
  <div class="default-layout__container">
    <navbar class="default-layout__navbar"/>
    <nuxt class="default-layout__nuxt"/>
    <hero class="default-layout__hero"/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'

export default {
  components: {
    Navbar,
    Hero
  }
}
</script>


<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: var(--secondary);
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

:root {
  --primary: #ffaa55;
  --secondary: #e1627d;
  --accent: #b16180;
}

.default-layout {
  &__container {
    display: flex;
    justify-content: space-between;
  }

  &__navbar {
    flex: 0 0 50px;
  }

  &__nuxt {
    flex: 1 1 45vw;
  }

  &__hero {
    flex: 0 0 50vw;
  }
}
</style>
