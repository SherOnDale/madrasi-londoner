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
        },
        {
          icon: 'snapchat',
          url: 'https://www.snapchat.com/add/iamjoel1996'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.hero {
  &__container {
    color: white;
    display: flex;
    flex-direction: column;
  }

  &__social {
    padding: 3rem 5rem 5rem 0;
    align-self: flex-end;
    display: flex;

    > * {
      margin-right: 1rem;
    }

    svg {
      height: 1.2rem;
      width: 1.2rem;
      fill: white;
    }
  }

  &__title,
  &__subtitle {
    align-self: center;
  }

  &__title {
    font-size: 3rem;
    font-weight: 300;
    margin-bottom: 1rem;

    .name {
      color: var(--primary);
      font-size: 4rem;
      font-weight: 700;
    }
  }

  &__subtitle {
    font-weight: 300;
    font-size: 2rem;
    margin-bottom: 2rem;
  }

  @media screen and (max-width: 1100px) {
    &__container {
      background: linear-gradient(
        135deg,
        var(--secondary),
        var(--accent) 35%,
        var(--secondary) 35%,
        var(--secondary) 65%,
        var(--accent) 65%,
        var(--secondary)
      );
    }

    &__social {
      padding: 1.5rem 0 1rem 0;
      align-self: center;
    }

    &__title {
      font-size: 2rem;

      .name {
        font-size: 2.5rem;
      }
    }

    &__subtitle {
      font-size: 1.5rem;
    }
  }
}
</style>
