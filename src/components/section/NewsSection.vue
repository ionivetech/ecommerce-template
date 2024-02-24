<script setup>
// Icons
import { ChevronRightIcon } from '@heroicons/vue/24/outline'

const newsList = [
  {
    image: 'news1',
    tag: 'Pet knowledge',
    title: 'What is a Pomeranian? How to Identify Pomeranian Dogs',
    description:
      'The Pomeranian, also known as the Pomeranian (Pom dog), is always in the top of the cutest pets. Not only that, the small, lovely, smart, friendly, and skillful circus dog breed.'
  },
  {
    image: 'news2',
    tag: 'Pet knowledge',
    title: 'Dog Diet You Need To Know',
    description:
      'Dividing a dogs diet may seem simple at first, but there are some rules you should know so that your dog can easily absorb the nutrients in the diet. For those who are just starting to raise dogs, especially newborn puppies with relatively weak resistance.'
  },
  {
    image: 'news3',
    tag: 'Pet knowledge',
    title: 'Why Dogs Bite and Destroy Furniture and How to Prevent It Effectively',
    description:
      'Dog bites are common during development. However, no one wants to see their furniture or important items being bitten by a dog.'
  }
]

const getImageUrl = (image) => {
  return new URL(`../../assets/images/news/${image}.webp`, import.meta.url)
}
</script>

<template>
  <section class="section">
    <!-- Header -->
    <div class="section__header">
      <div class="flex flex-col">
        <h3 class="section__header__subtitle">You already know ?</h3>
        <h2 class="section__header__title">Useful pet knowledge</h2>
      </div>

      <button class="btn btn--secondary d-none d-sm-flex">View more <ChevronRightIcon /></button>
    </div>

    <!-- List -->
    <div class="grid-list">
      <div
        v-for="list in newsList"
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
          <div class="card__tag">{{ list.tag }}</div>
          <div class="card__title">{{ list.title }}</div>
          <p class="card__description">{{ list.description }}</p>
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
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  grid-gap: 12px;

  @media screen and (min-width: 576px) {
    grid-template-columns: repeat(auto-fit, minmax(265px, 1fr));
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
