<template>
  <div
    class="relative w-full flex items-center justify-center bg-cover bg-center py-12 md:py-20"
    :style="{ backgroundImage: 'url(/kitchen.jpg)' }"
  >
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-55"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-6 md:py-20 px-4">
      <h1
        class="text-3xl md:text-5xl font-bold mb-2 drop-shadow-lg px-4 md:px-48"
      >
        San Antonio Custom Interiors
      </h1>
      <h1
        class="text-2xl md:text-4xl font-bold mb-8 md:mb-12 drop-shadow-lg px-4 md:px-48"
      >
        Kitchen, Bath, Cabinets, and More
      </h1>
      <p
        class="text-base md:text-xl max-w-2xl mx-auto font-medium text-gray-300 drop-shadow-lg mb-6 md:mb-8 px-4 md:px-0"
      >
        Styles by Design is your one stop shop for all your custom interior
        needs. We offer full kitchen &amp; bath remodels, custom cabinets,
        flooring and stone, 3D rendering, interior painting and more.
      </p>
      <p
        class="text-xl md:text-2xl max-w-2xl mx-auto drop-shadow-lg mb-4 font-bold px-4 md:px-0"
      >
        Contact us today for a free consultation!
      </p>
      <p
        class="text-2xl md:text-4xl max-w-2xl mx-auto drop-shadow-lg font-bold flex items-center justify-center gap-2"
      >
        <Phone class="phone-icon" size="32" /> 210-555-2928
      </p>
    </div>
  </div>
</template>

<script setup>
import { Phone } from "lucide-vue-next";
</script>

<style>
.hero-button-main {
  @apply mt-6 relative inline-block text-base sm:text-xl py-2 px-6 sm:py-3 md:px-10 cursor-pointer text-black font-bold rounded-md;
}

.phone-icon {
  margin-top: -8px;
  display: inline;
}
</style>
