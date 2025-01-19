<template>
  <!-- <section>
    <img src="@/assets/images/graddiv.jpg" class="w-full h-4 md:h-8" />
  </section> -->
  <footer class="bg-gray-900 text-white py-12">
    <div class="container mx-auto px-4 lg:px-0">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Section 1 -->
        <div>
          <h3 class="text-lg font-semibold mb-4">About Styles by Design</h3>
          <p class="text-sm text-gray-300 mb-4 leading-loose">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
          <p class="text-sm text-gray-300 mb-4 leading-loose">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>

        <!-- Section 2 (with Button) -->
        <div>
          <h3 class="text-lg font-semibold mb-4">Get in touch</h3>
          <p class="text-sm text-slate-300 mb-4 leading-loose">
            Free consultations available for all projects. Call us to schedule
            an appointment.
          </p>
          <p class="text-4xl font-bold text-center mt-8">
            <Phone size="32" class="phone-icon" /> 210-555-1039
          </p>

          <!-- <div class="text-center mt-8 mb-4">
            <button
              class="gradient-button-yellow text-blue-950 font-semibold py-2 px-6 rounded transition-all duration-300"
            >
              Join the mailing list
            </button>
          </div> -->
        </div>

        <!-- Section 3 -->
        <div>
          <h3 class="text-lg font-semibold mb-4">Follow us</h3>
          <p class="text-sm text-slate-300 mb-4 leading-loose">
            Connect with us on social media to see our latest projects and
            updates.
          </p>
          <ul class="flex flex-col">
            <li class="mb-4">
              <Twitter class="inline mr-2" />
              <a
                href="https://x.com/stylesbydesign"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                x.com/stylesbydesign
              </a>
            </li>
            <li class="mb-4">
              <Instagram class="inline mr-2" />
              <a
                href="https://instagram.com"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                instagram.com/stylesbydesign
              </a>
            </li>
            <li>
              <Youtube class="inline mr-2" />
              <a
                href="https://youtube.com"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                youtube.com/@stylesbydesign
              </a>
            </li>
          </ul>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="mt-12 text-center text-slate-600 text-sm">
        <p>&copy; {{ new Date().getFullYear() }} Styles by Design</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Twitter, Youtube, Instagram, Phone } from "lucide-vue-next";
</script>

<style>
footer {
  background: linear-gradient(
    195deg,
    #0e2223 0%,
    #0e2223 23%,
    #0e1c1b 40%,
    #152927 60%,
    #0e2223 85%,
    #0e2223 100%
  );
}

.phone-icon {
  margin-top: -8px;
  display: inline;
}
</style>
