<script setup>
// Icons
import { PlayCircleIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <section>
    <div class="banner">
      <div class="banner__accent-rectangle-1" />
      <div class="banner__accent-rectangle-2" />
      <img
        src="@/assets/images/img-banner-2.webp"
        width="382"
        height="349"
        alt="image-banner-2"
        class="banner__image"
      />

      <div class="banner__title">
        Adoption
        <img
          src="@/assets/icons/paw-icon.svg"
          width="42"
          height="38"
          alt="paw icon"
        />
      </div>
      <div class="banner__subtitle">We need help. so do they.</div>
      <p class="banner__description">
        Adopt a pet and give it a home, <br />
        andit will be love you back unconditionally.
      </p>

      <div class="banner__button">
        <button class="btn btn--primary">Explore Now</button>
        <button class="btn btn--secondary">View Intro <PlayCircleIcon /></button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.banner {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  height: 378px;
  padding: 50px 0px 50px 65px;
  background-color: #ffb775;
  border-radius: 20px;
  overflow: hidden;
  box-sizing: border-box;

  &__accent-rectangle-1 {
    position: absolute;
    transform: rotate(-35deg);
    left: -380px;
    top: -315px;
    width: 800px;
    height: 800px;
    border-radius: 80px;
    background-color: #fceed5;

    @media screen and (min-width: 1024px) {
      transform: rotate(-30deg);
      left: -340px;
      top: -350px;
    }
  }

  &__accent-rectangle-2 {
    position: absolute;
    transform: rotate(55deg);
    right: -250px;
    bottom: -600px;
    width: 800px;
    height: 800px;
    border-radius: 80px;
    background: linear-gradient(102.87deg, #fceed5 6.43%, #fceed5 78.33%, #ffe7ba 104.24%);
    opacity: 0.3;

    @media screen and (min-width: 1024px) {
      transform: rotate(60deg);
      right: -280px;
      bottom: -835px;
      width: 1000px;
      height: 1000px;
    }
  }

  &__image {
    position: absolute;
    right: -60px;
    top: 0;
    width: auto;
    height: 378px;

    @media screen and (min-width: 1024px) {
      right: -40;
    }
    @media screen and (min-width: 1140px) {
      right: 0;
    }
  }

  &__title {
    font-size: 36px;
    font-weight: 800;
    line-height: 54px;
    color: $primary;
    z-index: 1;
  }
  &__subtitle {
    font-size: 24px;
    font-weight: 700;
    line-height: 36px;
    color: $primary;
    z-index: 1;
  }
  &__description {
    max-width: 394px;
    font-size: 12px;
    font-weight: 500;
    line-height: 18px;
    letter-spacing: 0em;
    color: $neutral-dark;
    margin-top: 8px;
    z-index: 1;
  }
  &__button {
    margin-top: 42px;
    display: flex;
    align-items: center;
    gap: 16px;
    z-index: 1;
  }

  @media screen and (min-width: 1024px) {
    padding-left: 85px;

    &__title {
      font-size: 52px;
      line-height: 68px;
    }
    &__subtitle {
      font-size: 36px;
      line-height: 54px;
    }
  }
}
</style>
