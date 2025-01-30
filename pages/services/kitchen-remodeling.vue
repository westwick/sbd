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
  title: "Kitchen Remodeling",
  description:
    "Transform your kitchen into a stunning, functional space that reflects your style and meets your needs. Our comprehensive kitchen remodeling services combine expert craftsmanship with premium materials to create the kitchen of your dreams.",
  mainFeatures: [
    "Custom cabinet design and installation",
    "Premium countertop selection and installation",
    "Expert kitchen layout optimization",
    "Modern lighting and electrical updates",
    "High-quality flooring installation",
    "Professional appliance selection and installation",
  ],
  mainImage: "https://placehold.co/800x600",
  process: [
    {
      title: "Design Consultation",
      description:
        "We begin with a thorough consultation to understand your vision, needs, and budget. Our designers will help you explore options and create a detailed plan.",
    },
    {
      title: "Detailed Planning",
      description:
        "Our team develops comprehensive plans, including 3D renderings, material selections, and a detailed timeline for your project.",
    },
    {
      title: "Expert Installation",
      description:
        "Our skilled craftsmen handle every aspect of the installation, ensuring the highest quality results and attention to detail.",
    },
  ],
  galleryImages: [
    {
      src: "https://placehold.co/800x600",
      alt: "Modern Kitchen Design",
      description: "Contemporary kitchen with island",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Traditional Kitchen",
      description: "Classic design with modern amenities",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Luxury Kitchen",
      description: "High-end finishes and appliances",
    },
  ],
  faqs: [
    {
      question: "How long does a typical kitchen remodel take?",
      answer:
        "A typical kitchen remodel takes 6-8 weeks from demolition to completion. Timeline can vary based on the scope of work and material availability.",
    },
    {
      question: "Can I use my kitchen during the remodel?",
      answer:
        "We recommend setting up a temporary kitchen space during the remodel. We'll work with you to maintain access to essential appliances when possible.",
    },
    {
      question: "Do you handle all permits and inspections?",
      answer:
        "Yes, we handle all necessary permits and coordinate required inspections throughout the project.",
    },
  ],
};

useHead({
  title: "Kitchen Remodeling - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "Expert kitchen remodeling services in San Antonio. Custom cabinets, countertops, and complete renovations tailored to your style and budget.",
    },
  ],
});
</script>
