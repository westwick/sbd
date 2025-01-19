<template>
  <header class="px-2 md:px-4">
    <div
      class="container mx-auto flex flex-col md:flex-row items-center md:justify-between"
    >
      <div class="w-full md:w-auto flex justify-between items-center">
        <NuxtLink
          to="/"
          class="text-blue-900 text-lg md:text-xl font-bold flex items-center hover:text-blue-600"
          exact-active-class="text-blue-800"
        >
          <img src="@/assets/images/logosbd.jpg" class="logo mr-4" />
        </NuxtLink>

        <!-- Hamburger Button -->
        <button
          @click="isMenuOpen = !isMenuOpen"
          class="md:hidden p-2 text-cyan-700 hover:text-cyan-600"
        >
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              v-if="!isMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>

      <!-- Navigation Links Container -->
      <div
        class="w-full md:w-auto overflow-hidden md:overflow-visible transition-[max-height] duration-300 ease-out absolute md:relative left-0 right-0 top-[100%] bg-white md:bg-transparent shadow-lg md:shadow-none"
        :class="[isMenuOpen ? 'max-h-[400px]' : 'max-h-0 md:max-h-none']"
      >
        <div
          class="flex flex-col md:flex-row items-center space-y-2 md:space-y-0 md:space-x-4 mt-4 md:mt-0 pb-4 md:pb-0"
        >
          <NuxtLink
            v-for="(link, index) in navLinks"
            :key="index"
            :to="link.to"
            class="navlink text-cyan-700 text-md font-bold hover:text-cyan-600"
            exact-active-class="link-active text-cyan-500"
            @click="closeMenu"
          >
            {{ link.text }}
          </NuxtLink>
          <div
            v-if="index < navLinks.length - 1"
            class="text-slate-200 hidden md:block"
          >
            /
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { useRoute } from "vue-router";
import { computed, ref } from "vue";

const route = useRoute();
const isMenuOpen = ref(false);

const navLinks = [
  { to: "/services", text: "SERVICES" },
  { to: "/about", text: "ABOUT" },
  { to: "/gallery", text: "GALLERY" },
  { to: "/contact", text: "CONTACT" },
];

const closeMenu = () => {
  isMenuOpen.value = false;
};

const isAppsActive = computed(() => {
  return route.path.startsWith("/apps");
});
</script>

<style>
header {
  background: #fff;
  position: relative;
  z-index: 50;
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
  width: 300px;
  height: auto;
  padding-top: 16px;
  padding-bottom: 16px;
}

@media (min-width: 768px) {
  .logo {
    width: 400px;
  }
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

/* Navigation Menu Transition */
.nav-slide-enter-active,
.nav-slide-leave-active {
  transition: all 0.3s ease-out;
}

.nav-slide-enter-from,
.nav-slide-leave-to {
  opacity: 0;
  transform: translateY(-20px);
}

.nav-slide-enter-to,
.nav-slide-leave-from {
  opacity: 1;
  transform: translateY(0);
}

@media (min-width: 768px) {
  .nav-slide-enter-from,
  .nav-slide-leave-to,
  .nav-slide-enter-to,
  .nav-slide-leave-from {
    transform: none;
    opacity: 1;
  }
}
</style>
