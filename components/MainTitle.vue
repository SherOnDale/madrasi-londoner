<template>
  <div class="main-title">{{ title }}</div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title'
    }
  }
}
</script>

<style>
.main-title {
  width: max-content;
  font-size: 2rem;
  padding: 0 3rem 1rem 7rem;
  border-bottom: 0.1rem solid var(--primary);
  color: var(--primary);
}

@media screen and (max-width: 1100px) {
  .main-title {
    margin-top: 3rem;
    padding: 0 3rem 1rem 1rem;
  }
}
</style>
