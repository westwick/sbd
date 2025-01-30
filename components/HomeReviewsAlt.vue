<template>
  <div class="container mx-auto px-4 py-16 md:py-24">
    <h2 class="text-3xl font-bold text-center mb-16">What Our Customers Say</h2>

    <div
      class="flex flex-col md:flex-row justify-center items-center md:items-start gap-8 max-w-7xl mx-auto relative"
    >
      <!-- Test SVG -->
      <svg
        class="absolute inset-0 w-full h-full bg-blue-100"
        style="z-index: -1"
      >
        <rect x="0" y="0" width="100%" height="100%" fill="red" opacity="0.1" />
        <circle cx="50%" cy="50%" r="50" fill="blue" />
      </svg>

      <!-- Connecting lines (visible on md+ screens only) -->
      <svg
        class="absolute top-0 w-full h-40 hidden md:block pointer-events-none"
        style="z-index: 0"
      >
        <line
          x1="10%"
          y1="35%"
          x2="30%"
          y2="65%"
          stroke="#94A3B8"
          stroke-width="2"
          stroke-dasharray="4 4"
        />
        <line
          x1="30%"
          y1="65%"
          x2="50%"
          y2="35%"
          stroke="#94A3B8"
          stroke-width="2"
          stroke-dasharray="4 4"
        />
        <line
          x1="50%"
          y1="35%"
          x2="70%"
          y2="65%"
          stroke="#94A3B8"
          stroke-width="2"
          stroke-dasharray="4 4"
        />
        <line
          x1="70%"
          y1="65%"
          x2="90%"
          y2="35%"
          stroke="#94A3B8"
          stroke-width="2"
          stroke-dasharray="4 4"
        />
      </svg>

      <div
        v-for="(review, index) in reviews"
        :key="review.id"
        class="flex flex-col items-center text-center w-full md:w-1/5"
        :class="{
          'md:translate-y-16': index % 2 === 1,
        }"
      >
        <div class="group relative">
          <img
            :src="review.image"
            :alt="review.name"
            class="w-20 h-20 rounded-full object-cover mb-4 shadow-md transition-all duration-300 group-hover:scale-110 bg-white"
          />
        </div>
        <h3 class="font-semibold text-lg mb-2">{{ review.name }}</h3>
        <p class="text-gray-600">{{ review.text }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const reviews = [
  {
    id: 1,
    name: "Sarah J",
    text: "The best service I've experienced in years - absolutely transformed my business!",
    image: "https://i.pravatar.cc/150?img=1",
  },
  {
    id: 2,
    name: "Michael C",
    text: "Incredible attention to detail and outstanding customer support.",
    image: "https://i.pravatar.cc/150?img=2",
  },
  {
    id: 3,
    name: "Emma D",
    text: "Their innovative solutions helped us achieve our goals faster than expected.",
    image: "https://i.pravatar.cc/150?img=3",
  },
  {
    id: 4,
    name: "James W",
    text: "Exceeded all expectations - I couldn't be happier with the results.",
    image: "https://i.pravatar.cc/150?img=4",
  },
  {
    id: 5,
    name: "Lisa M",
    text: "Professional, efficient, and truly caring about their clients' success.",
    image: "https://i.pravatar.cc/150?img=5",
  },
];
</script>
