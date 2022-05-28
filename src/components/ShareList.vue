<template>
  <div class="share">
    <div v-if="!shareLink && !noLinks" class="share__explore">
      <span>Explore me</span>
      <button class="share__btn btn">
        <img src="@/assets/icons/open.svg" alt="open">
      </button>
    </div>
    <ul class="share__list">
      <li v-if="shareLink && !noLinks"  class="share__item">
        <a href="#" class="link" >
          Share
        </a>
      </li>
      <li class="share__item">
        <a href="#">
          <img src="@/assets/icons/facebook.svg" alt="FaceBook">
        </a>
      </li>
      <li class="share__item">
        <a href="#">
          <img src="@/assets/icons/github.svg" alt="GitHub">
        </a>
      </li>
      <li class="share__item">
        <a href="#">
          <img src="@/assets/icons/twitter.svg" alt="Twitter">
        </a>
      </li>
      <li class="share__item">
        <a href="#">
          <img src="@/assets/icons/linkedin.svg" alt="LinkedIn">
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ShareList',
  props: {
    shareLink: {
      type: Boolean,
      required: false
    },
    noLinks: {
      type: Boolean,
      required: false
    }
  }
}
</script>

<style lang="scss" scoped>
.share {
  margin-top: 3rem;
  padding-bottom: 1.5rem;

  &__explore {
    display: flex;
    column-gap: 1rem;
    align-items: center;
    margin-bottom: 27px;
  }

  &__btn {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--secondary-3);
    padding: 6px 8px;
  }

  &__list {
    display: flex;
    align-items: center;
  }

  &__item {
    margin-right: 24px;

    &:last-of-type {
      margin-right: 0;
    }
  }

  @media print {
    display: none;
  }
}
</style>
