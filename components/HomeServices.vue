<template>
  <div class="container mx-auto px-4 py-12 -mt-24 relative z-10">
    <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
      <!-- Service 1 -->
      <div
        class="flex flex-col items-center text-center bg-white p-2 rounded-lg shadow-lg"
      >
        <img
          src="https://placehold.co/300x200"
          alt="Interior Design"
          class="w-full rounded-lg mb-4"
        />
        <h3 class="font-bold text-xl mb-2">Kitchen Remodeling</h3>
        <p class="text-gray-600">
          Transform your space with our expert interior design services.
        </p>
        <p class="text-blue-500">Learn More</p>
      </div>

      <!-- Service 2 -->
      <div
        class="flex flex-col items-center text-center bg-white p-4 rounded-lg shadow-lg"
      >
        <img
          src="https://placehold.co/300x200"
          alt="Home Renovation"
          class="w-full rounded-lg mb-4"
        />
        <h3 class="font-bold text-xl mb-2">Bath Remodeling</h3>
        <p class="text-gray-600">
          Complete home makeovers tailored to your style and budget.
        </p>
      </div>

      <!-- Service 3 -->
      <div
        class="flex flex-col items-center text-center bg-white p-2 rounded-lg shadow-lg"
      >
        <img
          src="https://placehold.co/300x200"
          alt="Custom Furniture"
          class="w-full rounded-lg mb-4"
        />
        <h3 class="font-bold text-xl mb-2">Custom Furniture</h3>
        <p class="text-gray-600">
          Unique pieces designed and crafted for your space.
        </p>
      </div>

      <!-- Service 4 -->
      <div
        class="flex flex-col items-center text-center bg-white p-2 rounded-lg shadow-lg"
      >
        <img
          src="https://placehold.co/300x200"
          alt="Color Consulting"
          class="w-full rounded-lg mb-4"
        />
        <h3 class="font-bold text-xl mb-2">Color Consulting</h3>
        <p class="text-gray-600">
          Expert color schemes to enhance your home's atmosphere.
        </p>
      </div>
    </div>

    <!-- Additional Services Text -->
    <div class="text-center mt-8">
      <p class="text-gray-700 max-w-2xl mx-auto mb-3">
        Discover our full range of services including basement remodeling, home
        additions, outdoor living spaces, and more.
      </p>
      <router-link
        to="/services"
        class="text-blue-600 hover:text-blue-700 font-medium inline-block"
      >
        View all services →
      </router-link>
    </div>
  </div>
</template>
