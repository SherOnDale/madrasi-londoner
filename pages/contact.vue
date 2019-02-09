<template>
  <div class="contact">
    <main-title title="Contacts"/>
    <div class="contact__content">
      <contact-item icon-name="phone" contact-detail="+91 99 44 007900"/>
      <contact-item icon-name="email" contact-detail="iamjoel1996@gmail.com"/>
      <contact-item icon-name="location" contact-detail="My Address"/>
    </div>
  </div>
</template>

<script>
import MainTitle from '@/components/MainTitle.vue'
import ContactItem from '@/components/ContactItem.vue'

export default {
  components: {
    MainTitle,
    ContactItem
  }
}
</script>

<style lang="scss">
.contact {
  &__content {
    padding-left: 7rem;
    padding-top: 2.5rem;
    font-size: 1rem;
    line-height: 1.4rem;
    color: white;
  }

  @media screen and (max-width: 1100px) {
    &__content {
      padding-left: 1rem;
      padding-right: 1rem;
    }
  }
}
</style>
