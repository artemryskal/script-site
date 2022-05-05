<template>
  <div class="wrapper">
    <TheAside />
    <TheHeader />
    <TheArticle />
    <AddComment />
    <CommentsList />
    <AboutSection />
    <TheFooter />
  </div>
</template>

<script>
import TheAside from '@/components/TheAside'
import TheHeader from '@/components/TheHeader'
import TheArticle from '@/components/TheArticle'
import AddComment from '@/components/AddComment'
import CommentsList from '@/components/CommentsList'
import AboutSection from '@/components/AboutSection'
import TheFooter from '@/components/TheFooter'

export default {
  name: 'App',
  components: { TheAside, TheHeader, TheArticle, AddComment, CommentsList, AboutSection, TheFooter }
}
</script>

<style lang="scss">
@import '@/assets/scss/styles.scss';
</style>
