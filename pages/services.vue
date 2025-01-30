<template>
  <PageHeader subtitle="Services" title="Custom Interiors in San Antonio, TX" />

  <div class="container mx-auto px-4 py-16">
    <!-- Main Services -->
    <div class="space-y-24">
      <!-- Kitchen Remodeling -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
        <div class="space-y-6">
          <h2 class="text-3xl font-bold text-gray-900">Kitchen Remodeling</h2>
          <p class="text-lg text-gray-700">
            Transform your kitchen into a stunning, functional space. Our
            comprehensive kitchen remodeling services include custom cabinetry,
            countertop installation, lighting design, and complete renovations.
          </p>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Custom cabinet design and installation</li>
            <li>Countertop selection and installation</li>
            <li>Kitchen layout optimization</li>
            <li>Lighting and electrical updates</li>
            <li>Flooring installation</li>
            <li>Appliance selection and installation</li>
          </ul>
          <NuxtLink
            to="/services/kitchen-remodeling"
            class="inline-block bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition-colors"
          >
            Learn More
          </NuxtLink>
        </div>
        <div class="relative h-[400px] rounded-lg overflow-hidden shadow-xl">
          <img
            src="https://placehold.co/800x600"
            alt="Kitchen Remodeling"
            class="w-full h-full object-cover"
          />
        </div>
      </div>

      <!-- Bathroom Remodeling -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
        <div
          class="order-2 md:order-1 relative h-[400px] rounded-lg overflow-hidden shadow-xl"
        >
          <img
            src="https://placehold.co/800x600"
            alt="Bathroom Remodeling"
            class="w-full h-full object-cover"
          />
        </div>
        <div class="order-1 md:order-2 space-y-6">
          <h2 class="text-3xl font-bold text-gray-900">Bath Remodeling</h2>
          <p class="text-lg text-gray-700">
            Create your perfect bathroom oasis with our custom remodeling
            services. From luxury master baths to efficient guest bathrooms, we
            handle every aspect of the transformation.
          </p>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Custom shower and tub installation</li>
            <li>Tile design and installation</li>
            <li>Vanity and cabinet installation</li>
            <li>Plumbing fixtures and updates</li>
            <li>Lighting and electrical</li>
            <li>Accessibility modifications</li>
          </ul>
          <NuxtLink
            to="/services/bath-remodeling"
            class="inline-block bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition-colors"
          >
            Learn More
          </NuxtLink>
        </div>
      </div>

      <!-- Custom Cabinetry -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
        <div class="space-y-6">
          <h2 class="text-3xl font-bold text-gray-900">Custom Cabinetry</h2>
          <p class="text-lg text-gray-700">
            As certified Northville Cabinetry installers, we offer premium
            custom cabinet solutions for every room in your home. From kitchen
            cabinets to built-in entertainment centers.
          </p>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>Kitchen cabinets and islands</li>
            <li>Bathroom vanities</li>
            <li>Built-in entertainment centers</li>
            <li>Home office solutions</li>
            <li>Custom storage solutions</li>
            <li>Garage organization systems</li>
          </ul>
          <NuxtLink
            to="/services/custom-cabinetry"
            class="inline-block bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition-colors"
          >
            Learn More
          </NuxtLink>
        </div>
        <div class="relative h-[400px] rounded-lg overflow-hidden shadow-xl">
          <img
            src="https://placehold.co/800x600"
            alt="Custom Cabinetry"
            class="w-full h-full object-cover"
          />
        </div>
      </div>
    </div>

    <!-- Additional Services -->
    <div class="mt-32">
      <h2 class="text-3xl font-bold text-gray-900 mb-12 text-center">
        Additional Services
      </h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="service in additionalServices"
          :key="service.title"
          class="bg-white p-6 rounded-lg shadow-lg"
        >
          <h3 class="text-xl font-bold text-gray-900 mb-4">
            {{ service.title }}
          </h3>
          <p class="text-gray-700 mb-4">{{ service.description }}</p>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li v-for="feature in service.features" :key="feature">
              {{ feature }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const additionalServices = [
  {
    title: "Interior Painting",
    description:
      "Professional interior painting services with attention to detail and premium materials.",
    features: [
      "Color consultation",
      "Surface preparation",
      "Premium paints",
      "Clean and efficient",
    ],
  },
  {
    title: "Flooring Installation",
    description:
      "Expert installation of various flooring types to match your style and needs.",
    features: ["Hardwood", "Tile", "Luxury vinyl", "Laminate"],
  },
  {
    title: "Stone & Countertops",
    description:
      "Premium stone and countertop installation for kitchens and bathrooms.",
    features: ["Granite", "Quartz", "Marble", "Solid surface"],
  },
  {
    title: "3D Rendering",
    description:
      "Visualize your project before construction with our 3D rendering services.",
    features: [
      "Kitchen design",
      "Bathroom layouts",
      "Cabinet configurations",
      "Color visualization",
    ],
  },
  {
    title: "Home Additions",
    description:
      "Expand your living space with custom home additions and renovations.",
    features: [
      "Room additions",
      "Garage conversions",
      "Second story additions",
      "Outdoor living",
    ],
  },
  {
    title: "Project Management",
    description:
      "Full-service project management to ensure your renovation runs smoothly.",
    features: [
      "Timeline planning",
      "Contractor coordination",
      "Budget management",
      "Quality control",
    ],
  },
];

useHead({
  title: "Our Services - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "Explore our full range of interior design and remodeling services including kitchen & bath remodels, custom cabinetry, and more in San Antonio.",
    },
  ],
});
</script>
