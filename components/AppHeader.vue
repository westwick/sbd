<template>
  <header class="px-2 md:px-4">
    <div class="container mx-auto flex items-center justify-between">
      <NuxtLink
        to="/"
        class="text-blue-900 text-lg md:text-xl font-bold flex items-center hover:text-blue-600"
        exact-active-class="text-blue-800"
      >
        <img src="@/assets/images/logosbd.jpg" class="logo mr-4" />
      </NuxtLink>
      <div class="flex items-center space-x-4 ml-auto">
        <!-- <NuxtLink
          to="/"
          class="ml-4 navlink text-blue-900 text-md font-bold hover:text-blue-600"
          exact-active-class="link-active text-blue-800"
        >
          HOME
        </NuxtLink> -->
        <!-- <div class="text-slate-300">/</div> -->
        <NuxtLink
          to="/apps"
          class="navlink text-cyan-700 text-md font-bold hover:text-cyan-600"
          :class="{ 'link-active text-cyan-700': isAppsActive }"
        >
          SERVICES
        </NuxtLink>
        <div class="text-slate-200">/</div>
        <NuxtLink
          to="/apps"
          class="navlink text-cyan-700 text-md font-bold hover:text-cyan-600"
          :class="{ 'link-active text-cyan-700': isAppsActive }"
        >
          ABOUT
        </NuxtLink>
        <div class="text-slate-200">/</div>
        <NuxtLink
          to="/apps"
          class="navlink text-cyan-700 text-md font-bold hover:text-cyan-600"
          :class="{ 'link-active text-cyan-700': isAppsActive }"
        >
          GALLERY
        </NuxtLink>
        <div class="text-slate-200">/</div>
        <NuxtLink
          to="/contact"
          class="navlink text-cyan-700 text-md font-bold hover:text-cyan-600"
          exact-active-class="link-active text-cyan-700"
        >
          CONTACT
        </NuxtLink>
      </div>
    </div>
  </header>
</template>

<script setup>
import { useRoute } from "vue-router";
import { computed } from "vue";

const route = useRoute();

const isAppsActive = computed(() => {
  return route.path.startsWith("/apps");
});
</script>

<style>
header {
  background: #fff;
  position: relative;
}

header a {
  transition: all ease-in-out 0.2s;
}

.navlink {
  border-bottom: 3px solid transparent;
  border-top: 3px solid transparent;
  padding: 16px 8px;
  font-size: 20px;
}

.logo {
  width: 400px;
  height: auto;
  padding-top: 16px;
  padding-bottom: 16px;
}

/* .link-active {
  border-bottom: 3px solid #67a1d6;
  position: relative;
}

.link-active::before {
  content: "";
  position: absolute;
  left: 50%;
  bottom: -7px;
  transform: translateX(-50%);
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-top: 6px solid #67a1d6;
  z-index: 2;
} */
</style>
