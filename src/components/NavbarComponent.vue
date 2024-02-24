<script setup>
import { onMounted } from 'vue'

// Icons
import { Bars4Icon, MagnifyingGlassIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'

onMounted(() => {
  const navbar = document.getElementById('navbar')

  window.onscroll = function () {
    if (window.scrollY > 200) {
      navbar.classList.add('bg-white')
    } else {
      navbar.classList.remove('bg-white')
    }
  }
})
</script>

<template>
  <nav
    id="navbar"
    class="navbar"
  >
    <!-- Navbar mobile version -->
    <div class="navbar__mobile container">
      <Bars4Icon />
      <img
        src="@/assets/logo.svg"
        width="92"
        height="32"
        alt="application logo"
      />
      <MagnifyingGlassIcon />
    </div>

    <!-- Navbar desktop version -->
    <div class="navbar__desktop container">
      <div class="navbar__desktop__left-section">
        <img
          src="@/assets/logo.svg"
          width="92"
          height="32"
          alt="application logo"
        />

        <div class="navbar__desktop__left-section__menu">
          <a
            href="#"
            class="navbar__desktop__left-section__menu__list"
            >Home</a
          >
          <a
            href="#"
            class="navbar__desktop__left-section__menu__list"
            >Category</a
          >
          <a
            href="#"
            class="navbar__desktop__left-section__menu__list"
            >About</a
          >
          <a
            href="#"
            class="navbar__desktop__left-section__menu__list"
            >Contact</a
          >
        </div>
      </div>

      <div class="navbar__desktop__right-section">
        <!-- Search -->
        <div class="navbar-search">
          <MagnifyingGlassIcon />
          <input placeholder="Search something here!" />
        </div>

        <button class="btn btn--primary">Join the community</button>

        <div class="dropdown">
          <img
            src="@/assets/icons/country.svg"
            width="22"
            height="22"
            alt="country flag"
          />
          <span>VND</span>
          <ChevronDownIcon />
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  z-index: 100;
  background-color: transparent;
  width: 100%;
  height: 57px;

  @media screen and (min-width: 1024px) {
    height: 100px;
  }

  &__mobile {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    svg {
      width: 32px;
      height: 32px;
      cursor: pointer;
    }
    img {
      width: 92px;
      height: 32px;
    }

    @media screen and (min-width: 1024px) {
      display: none;
    }
  }

  &__desktop {
    display: none;
    height: 100%;
    align-items: center;
    justify-content: space-between;

    @media screen and (min-width: 1024px) {
      display: flex;
    }

    &__left-section {
      height: 100%;
      display: flex;
      align-items: center;

      img {
        margin-right: 48px;
      }
      &__menu {
        display: flex;
        align-items: center;
        gap: 48px;

        &__list {
          font-size: 16px;
          font-weight: 700;
          line-height: 24px;
          color: $primary;
        }
      }
    }

    &__right-section {
      height: 100%;
      display: flex;
      align-items: center;
    }
  }
}

.navbar-search {
  position: relative;
  width: 280px;
  max-width: 280px;
  margin-right: 14px;
  border: 1px solid #dddddd;
  border-radius: 9999px;

  input {
    box-sizing: border-box;
    width: 100%;
    padding: 12px 20px 12px 48px;
    border-radius: 9999px;
    background-color: #fdfdfd;
    border: none;

    &:focus {
      outline: none;
    }
  }

  svg {
    position: absolute;
    top: 9px;
    left: 14px;
    width: 20px;
    height: 20px;
    color: #667479;
  }
}

.dropdown {
  display: flex;
  align-items: center;
  gap: 6px;
  margin-left: 22px;
  cursor: pointer;

  span {
    font-size: 16px;
    font-weight: 500;
    line-height: 23px;
    color: $primary;
  }
  svg {
    width: 20px;
    height: 20px;
  }
}
</style>
