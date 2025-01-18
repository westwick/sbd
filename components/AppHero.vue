<template>
  <div
    class="relative w-full flex items-center justify-center bg-cover bg-center py-20"
    :style="{ backgroundImage: 'url(/kitchen.jpg)' }"
  >
    <!-- Solid overlay to dim the background -->
    <div class="absolute inset-0 bg-black opacity-50"></div>

    <!-- Content -->
    <div class="relative z-10 text-center text-white py-8 md:py-20 px-4">
      <h1 class="text-5xl md:text-5xl font-bold mb-2 drop-shadow-lg px-48">
        San Antonio Custom Interiors
      </h1>
      <h1 class="text-4xl md:text-4xl font-bold mb-12 drop-shadow-lg px-48">
        Kitchen, Bath, Cabinets, and More
      </h1>
      <p
        class="text-md md:text-xl max-w-2xl mx-auto font-medium text-slate-200 drop-shadow-lg"
      >
        Styles by Design is your one stop shop for all your custom interior
        needs. We offer full kitchen &amp; bath remodels, custom cabinets,
        flooring, and stone, 3d rendering, interior painting and more. Contact
        us today for a free consultation!
      </p>
    </div>
  </div>
</template>

<style>
.hero-button-main {
  @apply mt-6 relative inline-block text-base sm:text-xl py-2 px-6 sm:py-3 md:px-10 cursor-pointer text-black font-bold rounded-md;
}
</style>
