<template>
  <div class="container mx-auto px-4 py-8">
    <h2 class="text-3xl font-bold text-center mb-12">What Our Customers Say</h2>

    <div class="flex flex-col items-center gap-8">
      <!-- Top row: 3 reviews -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 w-full max-w-5xl">
        <div
          v-for="review in topRowReviews"
          :key="review.id"
          class="bg-white rounded-lg p-6 shadow-md transition-transform duration-300 hover:-translate-y-2"
        >
          <div class="flex flex-col items-center text-center">
            <img
              :src="review.image"
              :alt="review.name"
              class="w-20 h-20 rounded-full object-cover mb-4"
            />
            <h3 class="font-semibold text-lg mb-2">{{ review.name }}</h3>
            <p class="text-gray-600">{{ review.text }}</p>
          </div>
        </div>
      </div>

      <!-- Bottom row: 2 reviews -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full max-w-4xl">
        <div
          v-for="review in bottomRowReviews"
          :key="review.id"
          class="bg-white rounded-lg p-6 shadow-md transition-transform duration-300 hover:-translate-y-2"
        >
          <div class="flex flex-col items-center text-center">
            <img
              :src="review.image"
              :alt="review.name"
              class="w-20 h-20 rounded-full object-cover mb-4"
            />
            <h3 class="font-semibold text-lg mb-2">{{ review.name }}</h3>
            <p class="text-gray-600">{{ review.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const topRowReviews = [
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
];

const bottomRowReviews = [
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
