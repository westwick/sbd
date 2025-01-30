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
  title: "Custom Cabinetry",
  description:
    "As certified Northville Cabinetry installers, we provide premium custom cabinet solutions for every room in your home. From kitchen cabinets to entertainment centers, we create beautiful, functional storage that perfectly fits your space and style.",
  mainFeatures: [
    "Custom kitchen cabinets and islands",
    "Bathroom vanities and storage",
    "Built-in entertainment centers",
    "Home office solutions",
    "Mudroom and laundry organization",
    "Garage storage systems",
  ],
  mainImage: "https://placehold.co/800x600",
  process: [
    {
      title: "Design Consultation",
      description:
        "We assess your space and discuss your storage needs, style preferences, and budget to create the perfect custom solution.",
    },
    {
      title: "Custom Design",
      description:
        "Our designers create detailed plans and 3D renderings to help you visualize your custom cabinetry before production begins.",
    },
    {
      title: "Professional Installation",
      description:
        "Our certified installers ensure your custom cabinetry is perfectly fitted and finished to the highest standards.",
    },
  ],
  galleryImages: [
    {
      src: "https://placehold.co/800x600",
      alt: "Kitchen Cabinets",
      description: "Custom kitchen with premium finishes",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Entertainment Center",
      description: "Built-in entertainment solution",
    },
    {
      src: "https://placehold.co/800x600",
      alt: "Home Office",
      description: "Custom office storage and workspace",
    },
  ],
  faqs: [
    {
      question: "What cabinet lines do you offer?",
      answer:
        "We are certified Northville Cabinetry installers, offering their complete line of premium custom cabinets. We can accommodate various styles and budgets within their extensive collection.",
    },
    {
      question: "How long does custom cabinetry take?",
      answer:
        "Custom cabinetry typically takes 6-8 weeks from design approval to installation completion. This includes production time and professional installation.",
    },
    {
      question: "Do you offer financing options?",
      answer:
        "Yes, we offer various financing options to help make your custom cabinetry project more affordable. Ask about our current financing specials during your consultation.",
    },
  ],
};

useHead({
  title: "Custom Cabinetry - Styles by Design",
  meta: [
    {
      name: "description",
      content:
        "Premium custom cabinetry solutions in San Antonio. Certified Northville Cabinetry installers offering kitchen cabinets, entertainment centers, and storage solutions.",
    },
  ],
});
</script>
