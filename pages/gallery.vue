<template>
  <PageHeader subtitle="Gallery" title="Browse some of our recent projects" />

  <div class="container mx-auto px-4 py-16">
    <!-- Featured Projects with Before/After -->
    <div class="space-y-32">
      <!-- Project 1 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-start">
        <div class="md:col-span-1 space-y-4">
          <h2 class="text-3xl font-bold text-gray-900">
            Modern Kitchen Transformation
          </h2>
          <p class="text-lg text-gray-700">
            This Alamo Heights kitchen renovation showcases our commitment to
            blending functionality with elegant design. We transformed a dated
            1990s kitchen into a modern entertainment space, featuring custom
            cabinetry, quartz countertops, and a dramatic waterfall island.
          </p>
        </div>
        <div class="md:col-span-2">
          <BeforeAfterSlider
            :beforeImage="beforeImage"
            :afterImage="afterImage"
            beforeAlt="Kitchen Before Renovation"
            afterAlt="Kitchen After Renovation"
          />
        </div>
      </div>

      <!-- Project 2 -->
      <!-- <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-start">
        <div class="md:col-span-1 space-y-4">
          <h2 class="text-3xl font-bold text-gray-900">
            Luxury Master Bath Suite
          </h2>
          <p class="text-lg text-gray-700">
            This stunning master bathroom renovation in Shavano Park combines
            spa-like luxury with practical elegance. The project included custom
            tilework, a freestanding soaker tub, and a spacious walk-in shower
            with floor-to-ceiling glass.
          </p>
        </div>
        <div class="md:col-span-2">
          <BeforeAfterSlider
            beforeImage="https://placehold.co/1200x800"
            afterImage="https://placehold.co/1200x800"
            beforeAlt="Bathroom Before Renovation"
            afterAlt="Bathroom After Renovation"
          />
        </div>
      </div> -->

      <!-- Project 3 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-start">
        <div class="md:col-span-1 space-y-4">
          <h2 class="text-3xl font-bold text-gray-900">
            Custom Cabinet Installation
          </h2>
          <p class="text-lg text-gray-700">
            This whole-home cabinet project in Stone Oak showcases our custom
            woodworking expertise. From the kitchen to the home office, we
            created cohesive storage solutions that maximize space while
            maintaining aesthetic appeal.
          </p>
        </div>
        <div class="md:col-span-2">
          <BeforeAfterSlider
            beforeImage="https://placehold.co/1200x800"
            afterImage="https://placehold.co/1200x800"
            beforeAlt="Cabinets Before Installation"
            afterAlt="Cabinets After Installation"
          />
        </div>
      </div>
    </div>

    <!-- Additional Projects Grid -->
    <div class="mt-32">
      <h2 class="text-3xl font-bold text-gray-900 mb-12">
        More Project Highlights
      </h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(item, i) in galleryItems"
          :key="i"
          class="aspect-[4/3] relative overflow-hidden rounded-lg shadow-lg group"
        >
          <img
            :src="item.src"
            :alt="item.alt"
            class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div
            class="absolute inset-0 bg-black bg-opacity-40 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end"
          >
            <p class="text-white p-4 text-lg font-medium">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import BeforeAfterSlider from "@/components/BeforeAfterSlider.vue";

// Import images if they're in the assets directory
import beforeImage from "@/assets/images/photos/IMG_1068.jpg";
import afterImage from "@/assets/images/photos/IMG_1026.jpg";

const galleryItems = [
  {
    src: "https://placehold.co/800x600",
    alt: "Custom Kitchen Design",
    description: "Modern Kitchen with Island",
  },
  {
    src: "https://placehold.co/800x600",
    alt: "Bathroom Detail",
    description: "Luxury Shower Installation",
  },
  {
    src: "https://placehold.co/800x600",
    alt: "Cabinet Detail",
    description: "Custom Built-in Cabinets",
  },
  {
    src: "https://placehold.co/800x600",
    alt: "Kitchen Detail",
    description: "Quartz Countertop Installation",
  },
  {
    src: "https://placehold.co/800x600",
    alt: "Bathroom Vanity",
    description: "Double Vanity with Custom Mirror",
  },
  {
    src: "https://placehold.co/800x600",
    alt: "Kitchen Backsplash",
    description: "Designer Tile Backsplash",
  },
];

useHead({
  title: "Project Gallery - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "View our portfolio of custom interior projects including kitchen remodels, bathroom renovations, and custom cabinetry in San Antonio.",
    },
  ],
});
</script>

<style scoped>
.gallery-item img {
  @apply hover:scale-110;
}

.gallery-item:hover img {
  @apply scale-110;
}

/* Image Comparison Slider custom styles */
:deep(.img-comparison-slider) {
  @apply cursor-col-resize;
}

:deep(.img-comparison-slider [slot="second"]) {
  @apply cursor-e-resize;
}

:deep(.img-comparison-slider [slot="first"]) {
  @apply cursor-w-resize;
}
</style>
