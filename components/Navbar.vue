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

<style lang="scss">
.navbar {
  &__container {
    display: flex;
    flex-direction: column;
    height: 100vh;
    background-color: var(--secondary);
    background: linear-gradient(var(--accent), var(--secondary));
    border-right: 0.1rem solid var(--primary);
  }

  &__item {
    > .nuxt-link-exact-active {
      transition: all 0.5s;
      background-origin: content-box;
      background-color: var(--primary);

      svg {
        fill: black;
      }
    }
  }

  &__link {
    padding: 1rem 1.5rem;
    width: 100%;
    height: 100%;
    display: inline-block;

    svg {
      height: 2rem;
      width: 2rem;
      fill: var(--primary);
    }
  }

  @media screen and (max-width: 1100px) {
    &__container {
      flex-direction: row;
      border-right: 0;
      height: auto;
      border-bottom: 0.1rem solid var(--primary);
      justify-content: center;
    }

    &__link {
      padding: 0.5rem 1rem;
    }
  }
}
</style>
