<template>
  <section class="section container about">
    <h2 class="section__heading heading heading--h2">
      What I do!
    </h2>
    <p class="about__description">
      Mario Martin's love for storytelling originated as a young boy when he felt inspired to tell stories through writing. At eighteen he shot his first film, “Checkmate.” That was the birthing of his passion for film-making and screenwriting.
    </p>
    <p class="about__description">
      Early on he honed his craft at the Maine Media Workshops and Boston Film & Video Foundation.  Mario has attended many screenwriting boot-camps, worked with multiple coverage companies as well as many different screenwriters.
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
.about {
  @media print {
    margin-bottom: 2rem;
  }
}

.about__description {
  line-height: 1.5rem;
  margin-bottom: 1.5rem;

  &:last-of-type {
    margin-bottom: 0;
  }
}
</style>
