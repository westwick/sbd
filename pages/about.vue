<template>
  <PageHeader
    subtitle="About"
    title="Independently owned and family operated"
  />
  <div class="container mx-auto px-4 py-16">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
      <!-- Image Column -->
      <div class="relative">
        <img
          src="https://placehold.co/600x800"
          alt="Jon Styles"
          class="rounded-lg shadow-xl w-full object-cover"
        />
      </div>

      <!-- Content Column -->
      <div class="space-y-6">
        <h2 class="text-3xl font-bold text-gray-900">Meet Jon Styles</h2>
        <p class="text-lg text-gray-700 leading-relaxed">
          With over 20 years of experience in custom interior design and
          remodeling, Jon Styles has built a reputation for excellence in the
          San Antonio area. As the founder of Styles by Design, Jon brings his
          passion for craftsmanship and attention to detail to every project.
        </p>
        <p class="text-lg text-gray-700 leading-relaxed">
          Together with his wife Maria, Jon has created a family-operated
          business that treats every client like part of the family. Their
          commitment to quality and personal service has made Styles by Design
          one of San Antonio's most trusted names in custom interiors.
        </p>
        <div class="border-l-4 border-blue-500 pl-6 my-8">
          <p class="text-xl text-gray-800 italic">
            "Every home tells a story. Our job is to help you tell yours in the
            most beautiful way possible."
          </p>
          <p class="mt-2 text-gray-600">- Jon Styles</p>
        </div>
        <h3 class="text-2xl font-bold text-gray-900 mt-8">
          Community Involvement
        </h3>
        <p class="text-lg text-gray-700 leading-relaxed">
          Beyond their work in interior design, Jon and Maria are passionate
          advocates for children in the foster care system. As CASA (Court
          Appointed Special Advocates) volunteers, they dedicate their time to
          supporting and advocating for children navigating the foster care
          system in San Antonio.
        </p>
        <div class="mt-8 space-y-4">
          <h4 class="text-xl font-semibold text-gray-900">Certifications</h4>
          <ul class="list-disc list-inside text-gray-700 space-y-2">
            <li>
              Licensed Interior Designer - Texas Board of Architectural
              Examiners
            </li>
            <li>Certified Kitchen and Bath Designer</li>
            <li>Member of National Kitchen and Bath Association</li>
            <li>Certified Northville Cabinetry Installer</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: "About Jon Styles - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "Meet Jon Styles, founder of Styles by Design, bringing over 20 years of experience in custom interior design to San Antonio homes.",
    },
  ],
});
</script>
