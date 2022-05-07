<template>
  <header class="header container">
    <TheHeaderNav />

    <form action="#" method="get" class="form form--header">
      <label for="search" class="visually-hidden">
        Search
      </label>
      <input type="text" class="input" id="search" placeholder="Search">
      <button type="submit" class="btn btn--primary">
        <img src="@/assets/icons/search.svg" alt="Search ico">
      </button>
    </form>
  </header>
</template>

<script>
import TheHeaderNav from '@/components/TheHeaderNav'

export default {
  name: 'TheHeader',
  components: { TheHeaderNav }
}
</script>

<style lang="scss" scoped>
.header {
  margin-top: 3rem;

  @media (min-width: 1024px) {
    display: flex;
    align-items: flex-start;
    column-gap: 2%;
    margin-top: 0;
  }
  
  @media (min-width: 1440px) {
    padding: 0;
  }
}
</style>
