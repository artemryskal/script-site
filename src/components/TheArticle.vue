<template>
  <article class="article">
    <header class="container">
      <p class="description">
        User interface
      </p>
      <h1 class="article__heading heading">
        Bad Design vs. Good Design: 5 Examples We can Learn From
      </h1>
      <div class="article__info">
        <time datetime="2020-10-24" class="article__info-item description">October 24.2020</time>
        <a href="#" class="article__info-item description">Shane Hobbins</a>
      </div>
    </header>

    <picture>
      <source media="(max-width: 425px)" srcset="@/assets/images/article-img-320w.png">
      <source media="(min-width: 426px)" srcset="@/assets/images/article-img-733w.png">
      <img src="@/assets/images/article-img-733w.png" alt="Article cover" class="article__cover">
    </picture>

    <div class="article__text container">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. In mollis sagittis sem ac porta. Sed commodo ligula vitae mollis tristique. Maecenas egestas semper mauris. Duis tempus blandit ultrices. Proin elit nulla, viverra id suscipit quis, tristique a dolor. Sed dapibus, orci ac luctus tincidunt, massa erat porttitor odio, non imperdiet dui risus et elit.
      </p>
      <br>
      <p>
        Information overload
      </p>
      <br>
      <p>
        Vivamus dictum ultrices tortor. Ut imperdiet, enim in suscipit dignissim, mauris massa pellentesque augue, quis ultricies sem tortor et velit.
      </p>
      <blockquote class="article__blockquote">
        <p>
          Sed commodo ligula vitae mollis tristique. Maecenas egestas semper mauris. Duis tempus blandit ultrices. Proin elit nulla, viverra id suscipit quis, tristique a dolor.
        </p>
        <footer class="article__blockquote-footer">
          <cite>
            ‘Designing For Sustainability, Tim Frick, 2014'
          </cite>
        </footer>
      </blockquote>
      <section>
        <h3 class="article__inner-heading heading heading--h2">Lessons Learnt: Best Practice</h3>
        <ul class="article__list container">
          <li class="article__list-item">
            Morbi congue odio vel luctus aliquam. Morbi accumsan sapien at lorem ultricies aliquam eu eu nisl. Suspendisse.
          </li>
          <li class="article__list-item">
            Maecenas sit amet ligula auctor neque aliquam placerat et ac neque. Proin risus eros, fringilla eu suscipit dignissim, dignissim.
          </li>
        </ul>
      </section>
    </div>

    <ul class="article__tags container">
      <li class="article__tags-item">
        <a href="#" class="btn btn--tag">
          #HCI
        </a>
      </li>
      <li class="article__tags-item">
        <a href="#" class="btn btn--tag">
          #Design Thinking
        </a>
      </li>
    </ul>

    <ShareList class="article__share container" :shareLink="true"/>
  </article>
</template>

<script>
import ShareList from '@/components/ShareList'

export default {
  name: 'TheArticle',
  components: { ShareList }
}
</script>

<style lang="scss">
.article {
  margin-top: 4rem;

  &__heading {
    margin-top: 1.5rem;
  }

  &__info {
    display: flex;
    margin-top: 2.5rem;

    &-item {
      padding-right: 0.5rem;
      margin-right: 0.5rem;
      border-right: 1px solid var(--secondary-2);
      text-decoration: none;

      &:last-child {
        margin-right: 0;
        padding-right: 0;
        border-right: none;
      }
    }
  }

  &__cover {
    width: 100%;
    margin-top: 1.5rem;
    margin-bottom: 0.75rem;
  }

  &__text {
    font-size: 1.1rem;
    font-weight: 400;
    line-height: 2rem;
  }

  &__blockquote {
    padding-left: 1.5rem;
    border-left: 1px solid var(--secondary-2);
    margin: 2.5rem 0;
    font-size: 1rem;

    &-footer {
      margin-top: 2rem;
    }
  }

  &__inner-heading {
    margin: 2.5rem 0;
  }

  &__list {
    list-style: disc;
    font-size: 1rem;
  }

  &__list-item {
    margin-bottom: 2rem;

    &:last-of-type {
      margin-bottom: 0;
    }
  }

  &__tags {
    display: flex;
    column-gap: 4px;
    margin-top: 2.8rem;

    @media print {
      display: none;
    }
  }

  &__share {
    border-bottom: 1px solid var(--secondary-2);
  }

  @media print {
    margin-top: 0;
  }
}
</style>
