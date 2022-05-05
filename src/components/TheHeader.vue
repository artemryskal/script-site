<template>
  <header class="header container">
    <nav class="nav">
      <button class="nav__btn btn">
        <img src="@/assets/icons/burger.svg" alt="Burger Menu">
      </button>
    </nav>

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
export default {
  name: 'TheHeader'
}
</script>

<style lang="scss" scoped>
.header {
  margin-top: 3rem;
}

.nav {
  margin-bottom: 3rem;
  text-align: right;

  &__btn {
    padding: 9px 4px;
  }
}
</style>
