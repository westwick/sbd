<template>
  <div class="container mx-auto px-4 py-16">
    <!-- Hero Section -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-24">
      <div class="space-y-6">
        <h1 class="text-4xl font-bold text-gray-900">{{ title }}</h1>
        <p class="text-xl text-gray-700">{{ description }}</p>
        <ul class="list-disc list-inside text-gray-700 space-y-2">
          <li v-for="feature in mainFeatures" :key="feature">{{ feature }}</li>
        </ul>
      </div>
      <div class="relative h-[500px] rounded-lg overflow-hidden shadow-xl">
        <img :src="mainImage" :alt="title" class="w-full h-full object-cover" />
      </div>
    </div>

    <!-- Process Section -->
    <div class="mb-24">
      <h2 class="text-3xl font-bold text-gray-900 mb-12 text-center">
        Our Process
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div
          v-for="(step, index) in process"
          :key="index"
          class="bg-white p-8 rounded-lg shadow-lg"
        >
          <div class="text-3xl font-bold text-blue-600 mb-4">
            {{ index + 1 }}
          </div>
          <h3 class="text-xl font-bold text-gray-900 mb-4">{{ step.title }}</h3>
          <p class="text-gray-700">{{ step.description }}</p>
        </div>
      </div>
    </div>

    <!-- Gallery Section -->
    <div class="mb-24">
      <h2 class="text-3xl font-bold text-gray-900 mb-12 text-center">
        Recent Projects
      </h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(image, index) in galleryImages"
          :key="index"
          class="aspect-[4/3] relative overflow-hidden rounded-lg shadow-lg group"
        >
          <img
            :src="image.src"
            :alt="image.alt"
            class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-black bg-opacity-40 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white p-4 text-lg font-medium">
              {{ image.description }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- FAQ Section -->
    <div
      class="bg-gradient-to-t from-[rgb(215,223,232)] to-[rgb(244,246,248)] -mx-4 px-4 py-24"
    >
      <div class="container mx-auto">
        <h2 class="text-3xl font-bold text-gray-900 mb-12 text-center">
          Frequently Asked Questions
        </h2>
        <div class="max-w-3xl mx-auto space-y-6">
          <div
            v-for="(faq, index) in faqs"
            :key="index"
            class="bg-white rounded-lg shadow-lg p-6"
          >
            <h3 class="text-xl font-bold text-gray-900 mb-3">
              {{ faq.question }}
            </h3>
            <p class="text-gray-700">{{ faq.answer }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  mainFeatures: {
    type: Array,
    required: true,
  },
  mainImage: {
    type: String,
    required: true,
  },
  process: {
    type: Array,
    required: true,
  },
  galleryImages: {
    type: Array,
    required: true,
  },
  faqs: {
    type: Array,
    required: true,
  },
});
</script>
