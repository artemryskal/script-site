<template>
  <footer class="footer container">
    <div class="footer__wrapper wrapper">
      <p>Copyright © 2020 Meliora, Inc</p>
      <ShareList :noLinks="true" class="footer__share" />
      <button class="footer__btn btn" @click="scrollToTop">
        <img src="@/assets/icons/up.svg" alt="up">
      </button>
    </div>
  </footer>
</template>

<script>
import ShareList from '@/components/ShareList'

export default {
  name: 'TheFooter',
  components: { ShareList },
  setup () {
    const scrollToTop = () => {
      // For Safari
      document.body.scrollTop = 0
      // For others browsers
      document.documentElement.scrollTop = 0
    }

    return { scrollToTop }
  }
}
</script>

<style lang="scss" scoped>
.footer {
  position: relative;
  margin-top: 6.25rem;
  padding-top: 7.3rem;
  background-color: var(--secondary-3);
  font-size: 0.75rem;

  &__btn {
    position: absolute;
    top: -4px;
    left: 50%;
    width: 80px;
    height: 63px;
    transform: translate(-50%, -50%);
  }

  @media (min-width: 1024px) {
    padding-top: 2.5rem;
    padding-bottom: 2.5rem;

    &__wrapper {
      margin-top: 0;
      margin-bottom: 0;
      justify-content: space-between;
      align-items: center;
    }

    &__share {
      margin-top: 0;
      padding-bottom: 0;
    }
  }
}
</style>
