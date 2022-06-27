<template>
  <section class="section container">
    <h2 class="section__heading heading heading--h2">
      Comments
    </h2>
    <ul class="comments">
      <li v-for="(comment, index) in commentsList" :key="index" class="comments__item">
        <div class="comments__image">
          <img :src="require(`@/assets/images/${comment.img}`)" alt="Avatar">
        </div>
        <div class="comments__content">
          <div class="comments__info">
            <h3 class="heading heading--h2">
              {{ comment.name }}
            </h3>
            <span class="comments__time">
              {{ comment.time }}
            </span>
          </div>
          <p class="comments__text">
            {{ comment.text }}
          </p>
          <button class="comments__reply btn">
            <img src="@/assets/icons/reply.svg" alt="ico">
            Reply
          </button>

          <ul v-if="comment.list" class="comments">
            <li v-for="(item, i) in comment.list" :key="i" class="comments__item">
              <div class="comments__image">
                <img :src="require(`@/assets/images/${item.img}`)" alt="Avatar">
              </div>
              <div class="comments__content">
                <div class="comments__info">
                  <h3 class="heading heading--h2">
                    {{ item.name }}
                  </h3>
                  <span class="comments__time">
                    {{ item.time }}
                  </span>
                </div>
                <p class="comments__text">
                  {{ item.text }}
                </p>
                <button class="comments__reply btn">
                  <img src="@/assets/icons/reply.svg" alt="ico">
                  Reply
                </button>
              </div>
            </li>
          </ul>
        </div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'CommentsList',
  setup () {
    const commentsList = [
      {
        img: 'avatar-1.png',
        name: 'Jon Davis',
        time: '2 Minutes ago',
        text: 'Lorem ipsum dolor sit amet consectetuer adipiscing elit sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna',
        list: [
          {
            img: 'avatar-2.png',
            name: 'Shane Hobbins',
            time: 'Just now',
            text: 'Lorem ipsum dolor sit amet consectetuer adipiscing elit sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna',
          }
        ]
      },
      {
        img: 'avatar-1.png',
        name: 'Jon Davis',
        time: 'Just now',
        text: 'Lorem ipsum dolor sit amet consectetuer adipiscing elit sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna'
      }
    ]

    return { commentsList }
  }
}
</script>

<style lang="scss" scoped>
.comments {
  &__item {
    display: flex;
    padding-top: 1.5rem;
    border-bottom: 1px solid var(--secondary-2);
    page-break-inside: avoid;

    &:first-of-type {
      padding-top: 0;
    }

    &:last-of-type,
    & & {
      border-bottom: none;
    }
  }

  &__content {
    overflow: hidden;
  }

  &__image {
    min-width: 70px;
    margin-right: 1.5rem;
  }

  &__info {
    display: flex;
    flex-direction: column;
    row-gap: 8px;
  }

  &__time {
    margin-bottom: 1.5rem;
  }

  &__text {
    line-height: 2rem;
    font-size: 16px;
    font-weight: 400;
    margin-bottom: 1rem;
  }

  &__reply {
    margin-bottom: 2rem;

    @media print {
      display: none;
    }
  }
}
</style>
