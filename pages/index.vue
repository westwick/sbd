<template>
  <AppHero />
  <div class="bg-white">
    <section>
      <HomeServices />
    </section>
    <section
      class="bg-gradient-to-t from-[rgb(215,223,232)] to-[rgb(244,246,248)]"
    >
      <HomeApps />
    </section>
    <section>
      <HomeNews />
    </section>
    <section>
      <AppDiscounts />
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  meta: [
    {
      name: "description",
      content: "This is a custom page description for SEO and link previews.",
    },

    // Open Graph tags
    { property: "og:title", content: "Sugar Cube Studio" },
    {
      property: "og:description",
      content: "This is a custom page description for SEO and link previews.",
    },
    { property: "og:image", content: "https://example.com/og-image.jpg" }, // Replace with your image URL
    { property: "og:url", content: "https://sugarcubestudio.netlify.app/" },
    { property: "og:type", content: "website" },

    // Twitter Card tags
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "My Custom Page Title" },
    {
      name: "twitter:description",
      content: "This is a custom page description for SEO and link previews.",
    },
    { name: "twitter:image", content: "https://example.com/twitter-image.jpg" }, // Replace with your image URL
  ],
});
</script>

<style>
.angled-section {
  background: #1e1f33;
  position: relative;
  /* clip-path: polygon(
    -20px 0px,
    calc(100% + 20px) 0px,
    calc(100% - 100px) 100%,
    100px 100%
  ); */
  box-shadow: inset 0px 0px 20px 2px rgba(0, 0, 0, 10); /* Add shadow effect */
}
</style>
