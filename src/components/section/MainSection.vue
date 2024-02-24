<script setup>
// Icons
import { PlayCircleIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <section class="main-section">
    <div class="main-section__wrapper container">
      <h1 class="main-section__title">One More Friend</h1>
      <h2 class="main-section__subtitle">Thousands More Fun!</h2>
      <p class="main-section__description">
        Having a pet means you have more joy, a new friend, a happy person who will always be with
        you to have fun. We have 200+ different pets that can meet your needs!
      </p>

      <div class="main-section__button">
        <button class="btn btn--secondary">View Intro <PlayCircleIcon /></button>
        <button class="btn btn--primary">Explore Now</button>
      </div>

      <!-- Accent & image -->
      <div class="main-section__accent-rectangle-2" />
      <img
        src="@/assets/accent/rectangle.svg"
        alt="rectangle accent"
        width="30"
        height="30"
        class="main-section__accent-rectangle-sm"
      />
      <img
        src="@/assets/accent/rectangle-2.svg"
        alt="rectangle accent 2"
        width="30"
        height="30"
        class="main-section__accent-rectangle2-sm"
      />
      <img
        src="@/assets/accent/rectangle-2.svg"
        alt="rectangle accent 3"
        width="30"
        height="30"
        class="main-section__accent-rectangle3-sm"
      />
      <img
        src="@/assets/images/img-main-section-sm.webp"
        width="383"
        height="356"
        alt="image main section for mobile"
        class="main-section__image-sm"
      />
    </div>

    <!-- Accent and image -->
    <div class="main-section__accent-rectangle-1" />
    <img
      src="@/assets/images/img-main-section-lg.webp"
      width="383"
      height="356"
      alt="image main section for desktop"
      class="main-section__image-lg"
    />
  </section>
</template>

<style lang="scss" scoped>
.main-section {
  position: relative;
  height: 794px;
  background: linear-gradient(102.87deg, #fceed5 6.43%, #fceed5 78.33%, #ffe7ba 104.24%);
  margin-top: 0;
  margin-bottom: 40px;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  overflow: hidden;

  &__wrapper {
    position: relative;
    height: 100%;
    box-sizing: border-box;
    padding-top: 140px;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }

  &__title {
    font-size: 46px;
    font-weight: 800;
    line-height: 60px;
    color: $primary-dark;
    z-index: 1;
  }
  &__subtitle {
    font-size: 28px;
    font-weight: 700;
    line-height: 38px;
    color: $primary-dark;
    z-index: 1;
  }
  &__description {
    max-width: 382px;
    font-size: 12px;
    font-weight: 500;
    line-height: 18px;
    margin-top: 12px;
    color: $neutral-dark;
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
    height: 500px;
  }
  @media screen and (min-width: 1024px) {
    height: 695px;
    border-bottom-left-radius: 40px;
    border-bottom-right-radius: 40px;

    &__wrapper {
      padding-top: 180px;
    }
    &__title {
      font-size: 60px;
      line-height: 68px;
    }
    &__subtitle {
      font-size: 46px;
      line-height: 60px;
    }
    &__description {
      max-width: 480px;
      font-size: 16px;
      line-height: 24px;
      margin-top: 24px;
    }
  }

  // ========== Accent ==========
  &__accent-rectangle-1 {
    position: absolute;
    width: 600px;
    height: 600px;
    top: -550px;
    left: -225px;
    transform: rotate(20deg);
    background-color: $secondary-dark;
    border-radius: 80px;
  }
  &__accent-rectangle-2 {
    position: absolute;
    display: none;
    width: 635px;
    height: 635px;
    bottom: -635px;
    left: -95px;
    border-radius: 99px;
    opacity: 0.4px;
    transform: rotate(55deg);
    background-color: $secondary-dark;
    opacity: 0.4;

    @media screen and (min-width: 700px) {
      display: block;
    }
  }
  &__accent-rectangle-sm {
    position: absolute;
    top: 203px;
    left: 300px;
    width: 25px;
    height: 25px;
    transform: rotate(10deg);

    @media screen and (min-width: 1024px) {
      width: 30px;
      height: 30px;
      top: 228px;
      right: 42%;
      left: unset;
      transform: rotate(0deg) translateX(-50%);
    }
  }
  &__accent-rectangle2-sm {
    position: absolute;
    top: 179px;
    left: 347px;
    width: 25px;
    height: 25px;
    transform: rotate(-10deg);

    @media screen and (min-width: 1024px) {
      width: 15px;
      height: 15px;
      top: 180px;
      right: 41%;
      left: unset;
      transform: rotate(0deg) translateX(-50%);
    }
  }
  &__accent-rectangle3-sm {
    display: none;
    position: absolute;
    top: 140px;
    left: 6px;
    width: 60px;
    height: 60px;
    transform: rotate(-7deg);

    @media screen and (min-width: 800px) {
      display: block;
    }
    @media screen and (min-width: 1024px) {
      top: 175px;
      left: 6px;
      width: 75px;
      height: 75px;
    }
  }
  &__image-sm {
    position: absolute;
    left: 50%;
    bottom: -318px;
    transform: translateX(-30%);
    width: 700px;
    height: auto;
    border-bottom-right-radius: 20px;

    @media screen and (min-width: 700px) {
      display: none;
    }
  }
  &__image-lg {
    display: none;
    position: absolute;
    left: 50%;
    bottom: -318px;
    transform: translateX(-30%);
    width: 700px;
    height: auto;
    border-bottom-right-radius: 20px;

    @media screen and (min-width: 700px) {
      display: block;
      position: absolute;
      left: 68%;
      bottom: -208px;
      width: 550px;
    }
    @media screen and (min-width: 850px) {
      left: 80%;
      bottom: -239px;
      width: 650px;
      transform: translateX(-50%);
    }
    @media screen and (min-width: 1024px) {
      left: 76%;
      bottom: -296px;
      width: 800px;
      transform: translateX(-50%);
    }
    @media screen and (min-width: 1140px) {
      left: 70%;
      bottom: -326px;
      width: 900px;
      transform: translateX(-50%);
    }
  }
}
</style>
