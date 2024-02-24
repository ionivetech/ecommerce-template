<script setup>
// Components
import NavbarComponent from '@components/NavbarComponent.vue'
import MainSection from '@components/section/MainSection.vue'
import WhatsNewSection from '@components/section/WhatsNewSection.vue'
import OneMoreFriendBanner from '@components/banner/OneMoreFriendBanner.vue'
import OurProductSection from '@components/section/OurProductSection.vue'
import SellerSection from '@components/section/SellerSection.vue'
import AdoptionBanner from '@components/banner/AdoptionBanner.vue'
import NewsSection from '@components/section/NewsSection.vue'
import FooterComponent from '@components/FooterComponent.vue'
</script>

<template>
  <!-- Navbar -->
  <NavbarComponent />

  <!-- Main section -->
  <MainSection />

  <div class="container">
    <!-- Whats new -->
    <WhatsNewSection />

    <!-- One more friend banner -->
    <OneMoreFriendBanner />

    <!-- Our product -->
    <OurProductSection class="d-none d-sm-block" />

    <!-- Pet Seller -->
    <SellerSection class="d-none d-sm-block" />

    <!-- Adoption banner -->
    <AdoptionBanner class="d-none d-lg-block" />

    <!-- News -->
    <NewsSection />
  </div>

  <!-- Footer -->
  <FooterComponent />
</template>
