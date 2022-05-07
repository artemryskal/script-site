<template>
  <aside class="aside container">
    <a href="/" class="aside__link">
      <img src="@/assets/images/logo.png" alt="Logo" class="aside__logo">
    </a>
    
    <AboutSection class="aside__about" />
  </aside>
</template>

<script>
import AboutSection from './AboutSection.vue'

export default {
  name: 'TheAside',
  components: { AboutSection }
}
</script>


<style lang="scss" scoped>
.aside {
  text-align: center;

  &__about {
    display: none;
    text-align: left;

    @media (min-width: 1024px) {
      display: block;
    }
  }

  @media (min-width: 1024px) {
    max-width: 25%;
  }

  @media (min-width: 1440px) {
    padding: 0;
    margin-right: 6rem;
  }
}
</style>
