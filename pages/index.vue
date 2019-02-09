<template>
  <div class="about">
    <main-title title="About Me"/>
    <div class="about__content">
      <p>Hi I am a passionate and a budding Entrepreneur in the digital sector. I love to play with online advertising tools and learn the ever-changing trends in the digital sector. I have completed my Masters in Digital Marketing from Middlesex University, London, England. I received my undergraduate degree in Computer Science Engineering from Velammal college of engineering affiliated to Anna University, Chennai, India.</p> <p> The best part of my work is the ability where I can merge the engineering techniques in the field of online marketing. Some of the areas where I am strong is SEO, E-Marketing and Social Media management, Digital and Social media Analytics, Digital Advertising, Content building, Innovative planning, Strategy building. And this is my first ever brand for Digital Adverting, where u can learn some Digital Adverting based on the topic which you are interested to learn and I am also working on client’s brand/company/website/blog/individual for digital/online advertising based on the type of advertising in a very reasonable price. Join me to be a step ahead in digital sector.</p>
    </div>
  </div>
</template>

<script>
import MainTitle from '@/components/MainTitle.vue'

export default {
  components: {
    MainTitle
  }
}
</script>

<style lang="scss">
.about {
  &__content {
    padding-left: 7rem;
    padding-top: 2.5rem;
    font-size: 1rem;
    line-height: 1.4rem;
    color: white;

    p {
      margin-bottom: 1rem;
    }
  }
}
</style>
