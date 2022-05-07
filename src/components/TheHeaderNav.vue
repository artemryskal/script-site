<template>
  <nav class="nav">
    <button @click="toggleList" aria-expanded="false" aria-controls="nav-list" class="nav__btn btn" >
      <img src="@/assets/icons/burger.svg" alt="Burger Menu">
    </button>

    <ul class="nav__list" id="nav-list">
      <li v-for="(item, index) in itemsList" :key="index" class="nav__item">
        <a v-if="!item.list" :href="item.href" class="nav__link link">
          {{ item.name }}
        </a>
        <template v-else>
          <button aria-expanded="false" class="nav__link nav__link--list btn link" >
            {{ item.name }}
            <img src="@/assets/icons/arrow-bottom.svg" alt="ico" class="nav__ico">
          </button>
          <!-- <ul class="nav__list">
            <li v-for="(link, i) in item.list" :key="i" class="nav__item">
              <a :href="link.href" class="nav__link link">
                {{ link.name }}
              </a>
            </li> 
          </ul> -->
        </template>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'TheHeaderNav',
  setup() {
    const itemsList = [
      { name: 'Coverage', href: '#' },
      { name: 'Services', href: '#' },
      { name: 'Contact us', href: '#' },
      {
        name: 'More',
        href: '#',
        list: [
          { name: 'Inner 1', href: '#' },
          { name: 'Inner 2', href: '#' },
          { name: 'Inner 3', href: '#' }
        ]
      }
    ]

    const toggleList = (e) => {
      const expanded = e.currentTarget.getAttribute('aria-expanded') == 'true'
      e.currentTarget.setAttribute('aria-expanded', !expanded)
      e.currentTarget.nextElementSibling.classList.toggle('active')
    }

    return { itemsList, toggleList }
  }
}
</script>

<style lang="scss" scoped>
.nav {
  flex: 1;
  margin-bottom: 3rem;
  text-align: right;

  &__btn {
    padding: 9px 4px;

    @media (min-width: 1024px) {
      display: none;
    }
  }

  &__list {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.2s;

    @media (min-width: 1024px) {
      display: flex;
      justify-content: space-between;
      max-height: none;
    }

    & & {
      flex-direction: column;
      max-height: 0;
    }

    &.active {
      max-height: 300px;
      transition: max-height 0.5s;
    }
  }
  
  &__item {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;

    @media (min-width: 1024px) {
      margin-right: 2.8rem;
    }
  }

  &__link {
    position: relative;
    width: 100%;
    line-height: 2rem;
    color: var(--secondary-1);
    border: none;

    &::after {
      content: '';
      position: absolute;
      right: 0;
      bottom: 0;
      left: 0;
      height: 2px;
      background-color: rgba(0, 0, 0, 0);
      transition: 0.2s;
    }

    &:hover::after,
    &:focus::after {
      background-color: var(--secondary-1);
    }

    &--list {
      display: flex;
      justify-content: flex-end;
      align-items: center;
    }
  }

  &__ico {
    margin-left: 8px;
    transition: transform 0.4s;
  }

  &__link[aria-expanded=true] &__ico {
    transform: rotate(180deg)
  }
}
</style>
