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
  date() {
    return {
      svg: svg
    }
  }
}
</script>

<style>
</style>
