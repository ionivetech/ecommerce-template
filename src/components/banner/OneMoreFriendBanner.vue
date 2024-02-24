<script setup>
// Icons
import { PlayCircleIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <section>
    <div class="banner">
      <div class="banner__title">One more friend</div>
      <div class="banner__subtitle">Thousands more fun!</div>
      <p class="banner__description">
        Having a pet means you have more joy, a new friend, a happy person who will always be with
        you to have fun. We have 200+ different pets that can meet your needs!
      </p>

      <div class="banner__button">
        <button class="btn btn--secondary">View Intro <PlayCircleIcon /></button>
        <button class="btn btn--primary">Explore Now</button>
      </div>

      <!-- Accent and image -->
      <div class="banner__accent-rectangle-1" />
      <div class="banner__accent-rectangle-2" />
      <img
        src="@/assets/images/img-banner-1.webp"
        width="382"
        height="349"
        alt="image-banner-1"
        class="banner__image"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.banner {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 640px;
  padding: 40px 16px 0 16px;
  background-color: $primary;
  border-radius: 20px;
  overflow: hidden;
  box-sizing: border-box;

  &__title {
    font-size: 36px;
    font-weight: 800;
    line-height: 54px;
    text-align: center;
    color: $primary;
    z-index: 1;
  }
  &__subtitle {
    font-size: 24px;
    font-weight: 700;
    line-height: 36px;
    text-align: center;
    color: $primary;
    z-index: 1;
  }
  &__description {
    max-width: 342px;
    font-size: 12px;
    font-weight: 500;
    line-height: 18px;
    letter-spacing: 0em;
    text-align: center;
    color: $neutral-dark;
    margin-top: 12px;
    z-index: 1;
  }
  &__button {
    margin-top: 32px;
    display: flex;
    align-items: center;
    gap: 16px;
    z-index: 1;
  }

  @media screen and (min-width: 700px) {
    height: 740px;
  }
  @media screen and (min-width: $large) {
    height: 378px;
    align-items: flex-end;
    justify-content: center;
    padding-right: 45px;
  }
  @media screen and (min-width: 1024px) {
    &__title {
      font-size: 52px;
      line-height: 68px;
    }
    &__subtitle {
      font-size: 36px;
      line-height: 54px;
    }
    &__description {
      text-align: right;
    }
  }
  @media screen and (min-width: 1140px) {
    padding-right: 85px;
  }

  &__accent-rectangle-1 {
    position: absolute;
    top: -470px;
    left: -335px;
    width: 800px;
    height: 800px;
    background-color: #fceed5;
    transform: rotate(10deg);
    z-index: 0;
    border-radius: 100px;

    @media screen and (min-width: 470px) {
      left: -144px;
    }
    @media screen and (min-width: 700px) {
      top: -615px;
      left: -9px;
      width: 1000px;
      height: 1000px;
    }
    @media screen and (min-width: $large) {
      transform: rotate(-55deg);
      left: unset;
      right: -435px;
      top: -276px;
      width: 800px;
      height: 800px;
      border-radius: 80px;
    }
    @media screen and (min-width: 1024px) {
      right: -400px;
      top: -280px;
    }
    @media screen and (min-width: 1140px) {
      right: -300px;
    }
  }

  &__accent-rectangle-2 {
    position: absolute;
    bottom: -700px;
    left: -170px;
    width: 800px;
    height: 800px;
    background-color: #002a48;
    transform: rotate(25deg);
    z-index: 0;
    border-radius: 100px;

    @media screen and (min-width: 470px) {
      left: -180px;
      bottom: -645px;
    }
    @media screen and (min-width: 700px) {
      bottom: -835px;
      left: -211px;
      width: 1000px;
      height: 1000px;
    }
    @media screen and (min-width: $large) {
      bottom: -610px;
      left: -240px;
      width: 800px;
      height: 800px;
      border-radius: 80px;
      transform: rotate(35deg);
    }
    @media screen and (min-width: 1024px) {
      bottom: -585px;
      left: -250px;
    }
  }

  &__image {
    position: absolute;
    left: 50%;
    bottom: 0;
    transform: translateX(-50%);
    width: 370px;
    height: auto;

    @media screen and (min-width: 470px) {
      width: 392px;
    }
    @media screen and (min-width: 700px) {
      width: 500px;
    }
    @media screen and (min-width: $large) {
      transform: unset;
      left: 40px;
      width: 382px;
    }
    @media screen and (min-width: 1024px) {
      width: 400px;
    }
  }
}
</style>
