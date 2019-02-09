<template>
  <div class="default-layout__container">
    <navbar class="default-layout__navbar"/>
    <main class="default-layout__main">
      <div class="default-layout__main--spacer"/>
      <nuxt/>
    </main>
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
  background: linear-gradient(
      135deg,
      var(--secondary),
      var(--accent) 25%,
      transparent 25%,
      transparent 75%,
      var(--accent) 75%,
      var(--secondary)
    ),
    linear-gradient(var(--secondary), var(--accent));
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
  --breakpoint-md: 1100px;
}

::selection {
  color: var(--primary);
  background: var(--secondary);
}

.default-layout {
  &__container {
    display: flex;
    justify-content: space-between;
  }

  &__navbar {
    flex: 0 0 50px;
  }

  &__main {
    flex: 1 1 45vw;
    display: flex;
    flex-direction: column;
    padding-bottom: 10rem;

    &--spacer {
      flex-grow: 1;
    }
  }

  &__hero {
    flex: 0 0 50vw;
  }
}

@media screen and (max-width: 1100px) {
  html {
    background: var(--secondary);
  }

  .default-layout {
    &__container {
      flex-direction: column;
    }

    &__main {
      order: 1;
      flex: initial;
    }

    &__navbar {
      flex: initial;
    }

    &__hero {
      flex: initial;
    }
  }
}
</style>
