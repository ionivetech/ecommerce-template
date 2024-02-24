<script setup>
// Icons
import { ChevronRightIcon } from '@heroicons/vue/24/outline'

const productList = [
  {
    image: 'product1',
    title: 'Reflex Plus Adult Cat Food Salmon',
    product: 'Dog Food',
    size: '385gm',
    price: '140.000',
    free: 'Free Toy & Free Shaker'
  },
  {
    image: 'product2',
    title: 'Reflex Plus Adult Cat Food Salmon',
    product: 'Cat Food',
    size: '1.5kg',
    price: '165.000',
    free: 'Free Toy & Free Shaker'
  },
  {
    image: 'product3',
    title: 'Cat scratching ball toy kitten sisal rope ball',
    product: 'Toy',
    size: '',
    price: '1.100.000',
    free: 'Free Cat Food'
  },
  {
    image: 'product4',
    title: 'Cute Pet Cat Warm Nest',
    product: 'Toy',
    size: '',
    price: '410.000',
    free: 'Free Cat Food'
  },
  {
    image: 'product5',
    title: 'NaturVet Dogs - Omega-Gold Plus Salmon Oil',
    product: 'Dog Food',
    size: '385gm',
    price: '350.000',
    free: 'Free Toy & Free Shaker'
  },
  {
    image: 'product6',
    title: 'Costumes Fashion Pet Clother Cowboy Rider',
    product: 'Costume',
    size: '1.5kg',
    price: '500.000',
    free: 'Free Toy & Free Shaker'
  },
  {
    image: 'product7',
    title: 'Costumes Chicken Drumsti ck Headband',
    product: 'Costume',
    size: '',
    price: '400.000',
    free: 'Free Cat Food'
  },
  {
    image: 'product8',
    title: 'Plush Pet Toy',
    product: 'Toy',
    size: '',
    price: '250.000',
    free: 'Free Toy & Free Shaker'
  }
]

const getImageUrl = (image) => {
  return new URL(`../../assets/images/products/${image}.webp`, import.meta.url)
}
</script>

<template>
  <section class="section">
    <!-- Header -->
    <div class="section__header">
      <div class="flex flex-col">
        <h3 class="section__header__subtitle">Hard to choose right products for your pets?</h3>
        <h2 class="section__header__title">Our Products</h2>
      </div>

      <button class="btn btn--secondary">View more <ChevronRightIcon /></button>
    </div>

    <!-- List -->
    <div class="grid-list">
      <div
        v-for="list in productList"
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
              Product: <b>{{ list.product }}</b>
            </div>
            <div
              v-if="list.size"
              class="card__detail__list"
            >
              Size: <b>{{ list.size }}</b>
            </div>
          </div>

          <div class="card__price">{{ list.price }} VND</div>

          <div class="card__gift-banner">
            <img
              src="@/assets/icons/gift.svg"
              width="20"
              height="20"
              :alt="`gift-icon-${list.image}`"
            />
            <div class="card__gift-banner__text">{{ list.free }}</div>
          </div>
        </div>
      </div>
    </div>
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
