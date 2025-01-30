<template>
  <ServiceDetail
    :title="serviceData.title"
    :description="serviceData.description"
    :mainFeatures="serviceData.mainFeatures"
    :mainImage="serviceData.mainImage"
    :process="serviceData.process"
    :galleryImages="serviceData.galleryImages"
    :faqs="serviceData.faqs"
  />
</template>

<script setup>
import ServiceDetail from "@/components/ServiceDetail.vue";

const serviceData = {
  title: "Bath Remodeling",
  description:
    "Create your perfect bathroom sanctuary with our expert remodeling services. From luxurious master suites to efficient guest bathrooms, we combine beautiful design with practical functionality to transform your space.",
  mainFeatures: [
    "Custom shower and tub installations",
    "Premium tile design and installation",
    "Vanity and storage solutions",
    "Modern lighting and fixtures",
    "Plumbing updates and repairs",
    "Accessibility modifications",
  ],
  mainImage: "https://placehold.co/800x600",
  process: [
    {
      title: "Initial Consultation",
      description:
        "We meet to discuss your vision, requirements, and budget. Our designers help you explore styles and materials that match your preferences.",
    },
    {
      title: "Design & Planning",
      description:
        "We create detailed designs and 3D renderings, select materials, and develop a comprehensive project timeline.",
    },
    {
      title: "Professional Installation",
      description:
        "Our experienced team handles the complete installation with attention to detail and quality craftsmanship.",
    },
  ],
  galleryImages: [
    {
      src: "https://placehold.co/800x600",
      alt: "Luxury Master Bath",
      description: "Spa-like master bathroom retreat",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Modern Shower Design",
      description: "Custom tile work and glass enclosure",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Guest Bathroom",
      description: "Efficient and stylish guest bath",
    },
  ],
  faqs: [
    {
      question: "How long does a bathroom remodel typically take?",
      answer:
        "A standard bathroom remodel usually takes 3-4 weeks. Master bathrooms or more complex projects may take 6-8 weeks.",
    },
    {
      question: "Do you provide temporary facilities during the remodel?",
      answer:
        "For homes with multiple bathrooms, we coordinate the project to maintain access to other facilities. For single-bathroom homes, we can discuss temporary solution options.",
    },
    {
      question: "Are your bathroom remodels waterproof?",
      answer:
        "Yes, we use industry-leading waterproofing systems and techniques to ensure your bathroom is properly sealed and protected from water damage.",
    },
  ],
};

useHead({
  title: "Bath Remodeling - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "Expert bathroom remodeling services in San Antonio. Custom showers, vanities, and complete renovations for your perfect bathroom sanctuary.",
    },
  ],
});
</script>
