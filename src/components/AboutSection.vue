<template>
  <section class="section container about">
    <h2 class="section__heading heading heading--h2">
      What I do!
    </h2>
    <p class="about__description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer aliquet, orci in bibendum luctus, turpis ante pretium velit, eu rutrum augue erat ac eros. Cras ultricies mattis convallis. Nullam non turpis eget sapien mattis eleifend non vel tortor. Maecenas at nibh ipsum. Integer. 
    </p>

    <ShareList />
  </section>
</template>

<script>
import ShareList from '@/components/ShareList'

export default {
  name: 'AboutSection',
  components: { ShareList }
}
</script>

<style lang="scss" scoped>
.about__description {
  line-height: 1.5rem;
}
</style>
