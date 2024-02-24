<script setup>
// Icons
import { ChevronRightIcon } from '@heroicons/vue/24/outline'

const newLists = [
  {
    image: 'pets1',
    title: 'MO231 - Pomeranian White',
    gene: 'Male',
    age: '02',
    price: '4.000.000'
  },
  {
    image: 'pets2',
    title: 'MO502 - Poodle Tiny Yellow',
    gene: 'Female',
    age: '02',
    price: '3.900.000'
  },
  {
    image: 'pets3',
    title: 'MO102 - Poodle Tiny Sepia',
    gene: 'Male',
    age: '02',
    price: '4.000.000'
  },
  {
    image: 'pets4',
    title: 'MO512 - Alaskan Malamute Grey',
    gene: 'Male',
    age: '02',
    price: '8.900.000'
  },
  {
    image: 'pets5',
    title: 'MO231 - Pembroke Corgi Cream',
    gene: 'Male',
    age: '02',
    price: '7.900.000'
  },
  {
    image: 'pets6',
    title: 'MO502 - Pembroke Corgi Tricolor',
    gene: 'Female',
    age: '02',
    price: '9.000.000'
  },
  {
    image: 'pets7',
    title: 'MO231 - Pomeranian White',
    gene: 'Female',
    age: '02',
    price: '6.500.000'
  },
  {
    image: 'pets8',
    title: 'MO512 - Poodle Tiny Dairy Cow',
    gene: 'Male',
    age: '02',
    price: '5.000.000'
  }
]

const getImageUrl = (image) => {
  return new URL(`../../assets/images/pets/${image}.webp`, import.meta.url)
}
</script>

<template>
  <section class="section">
    <!-- Header -->
    <div class="section__header">
      <div class="flex flex-col">
        <h3 class="section__header__subtitle">Whats new?</h3>
        <h2 class="section__header__title">Take a look at some of our pets</h2>
      </div>

      <button class="btn btn--secondary d-none d-sm-flex">View more <ChevronRightIcon /></button>
    </div>

    <!-- List -->
    <div class="grid-list">
      <div
        v-for="list in newLists"
        :key="list.image"
        class="card"
      >
        <img
          :src="getImageUrl(list.image)"
          :alt="list.title"
          width="169"
          height="169"
          class="card__image"
        />

        <div class="card__detail-wrapper">
          <div class="card__title">{{ list.title }}</div>

          <div class="card__detail">
            <div class="card__detail__list">
              Gene: <b>{{ list.gene }}</b>
            </div>
            <div class="card__detail__list">
              Age: <b>{{ list.age }} month</b>
            </div>
          </div>

          <div class="card__price">{{ list.price }} VND</div>
        </div>
      </div>
    </div>

    <button
      class="btn btn--secondary btn--block d-sm-none"
      style="margin-top: 16px"
    >
      View more <ChevronRightIcon />
    </button>
  </section>
</template>

<style lang="scss" scoped>
.grid-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(175px, 1fr));
  grid-gap: 12px;

  @media screen and (min-width: 576px) {
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    grid-gap: 20px;
  }
}

.card__image {
  width: 100%;
  height: 169px;
  object-fit: cover;
  border-radius: 10px;
  margin-bottom: 8px;

  @media screen and (min-width: 576px) {
    height: 264px;
  }
}
</style>
