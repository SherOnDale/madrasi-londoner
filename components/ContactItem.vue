<template>
  <div class="contact-item">
    <div class="contact-item__icon" v-html="svg[iconName]"/>
    <div class="contact-item__text">{{ contactDetail }}</div>
  </div>
</template>

<script>
import svg from '@/assets/svg.js'
export default {
  props: {
    iconName: {
      type: String,
      default: 'person'
    },
    contactDetail: {
      type: String,
      default: 'Contact Detail'
    }
  },
  data() {
    return {
      svg
    }
  }
}
</script>

<style lang="scss">
.contact-item {
  display: flex;
  align-items: center;
  margin-bottom: 1.5rem;

  &__icon {
    height: 1rem;
    width: 1rem;
    margin-right: 1rem;

    svg {
      height: 1rem;
      width: 1rem;
      fill: var(--primary);
    }
  }
}
</style>
