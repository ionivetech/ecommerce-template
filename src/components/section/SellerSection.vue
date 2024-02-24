<script setup>
// Icons
import { ChevronRightIcon } from '@heroicons/vue/24/outline'

const sellerList = [
  {
    image: 'seller1',
    alt: 'Sheba'
  },
  {
    image: 'seller2',
    alt: 'Whiskas'
  },
  {
    image: 'seller3',
    alt: 'Bakers'
  },
  {
    image: 'seller4',
    alt: 'Felix'
  },
  {
    image: 'seller5',
    alt: 'Good Boy'
  },
  {
    image: 'seller6',
    alt: 'Butchers'
  },
  {
    image: 'seller7',
    alt: 'Pedigree'
  }
]

const getImageUrl = (image) => {
  return new URL(`../../assets/images/sellers/${image}.webp`, import.meta.url)
}
</script>

<template>
  <section class="section">
    <!-- Header -->
    <div class="section__header">
      <div
        class="flex items-center"
        style="gap: 8px"
      >
        <h3 class="section__header__subtitle">Proud to be part of</h3>
        <h2 class="section__header__title">Pet Sellers</h2>
      </div>

      <button class="btn btn--secondary d-none d-sm-flex">
        View all our sellers <ChevronRightIcon />
      </button>
    </div>

    <div class="seller-list">
      <img
        v-for="seller in sellerList"
        :key="seller.alt"
        :src="getImageUrl(seller.image)"
        width="152"
        height="112"
        :alt="seller.alt"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.seller-list {
  display: flex;
  gap: 20px;
  overflow-x: auto;

  -ms-overflow-style: none;
  scrollbar-width: none;

  &::-webkit-scrollbar {
    display: none;
  }
}
</style>
