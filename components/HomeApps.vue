<template>
  <div
    class="bg-city py-16 relative overflow-hidden"
    :style="{ backgroundImage: `url(${mapBackground})` }"
  >
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row items-center">
        <div
          class="w-full md:w-1/2 md:order-1 order-2 relative h-64 md:h-96 mt-8 md:mt-0"
        >
          <!-- <img
            src="@/assets/images/mapsa.jpg"
            alt="Service Area Map"
            class="w-full h-full object-cover rounded-lg"
          /> -->
        </div>
        <div
          class="w-full px-8 pb-32 md:pb-0 md:px-0 md:w-1/2 md:pl-8 order-1 md:order-2"
        >
          <div class="areas-we-serve">
            <h2 class="text-2xl font-bold mb-6 text-black">Areas We Serve</h2>
            <div class="two-column-list">
              <ul>
                <li>Alamo Heights</li>
                <li>Boerne</li>
                <li>Bulverde</li>
                <li>Canyon Lake</li>
                <li>Cibolo</li>
                <li>Devine</li>
                <li>Fair Oaks Ranch</li>
                <li>Hollywood Park</li>
                <li>Helotes</li>
                <li>Kerrville</li>
                <li>Kirby</li>
                <li>Leon Springs</li>
              </ul>
              <ul>
                <li>Live Oak</li>
                <li>Marion</li>
                <li>New Braunfels</li>
                <li>Pipe Creek</li>
                <li>San Antonio</li>
                <li>Schertz</li>
                <li>Seguin</li>
                <li>Selma</li>
                <li>Shavano Park</li>
                <li>Spring Branch</li>
                <li>St. Hedwig</li>
                <li>Universal City</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import mapBackground from "@/assets/images/mapsa.jpg";
</script>

<style scoped>
.two-column-list {
  display: flex;
  justify-content: space-between;
  max-width: 800px;
  margin: 0 auto;
  gap: 2rem;
}

.two-column-list ul {
  list-style-type: disc;
  padding-left: 1.5rem;
  margin: 0;
  min-width: 200px;
}

.two-column-list li {
  margin-bottom: 0.5rem;
  text-align: left;
}

@media (max-width: 768px) {
  .two-column-list {
    flex-direction: column;
    gap: 1rem;
  }
}

.bg-city {
  background-position-x: -71%;
  background-position-y: 31%;
  background-repeat: no-repeat;
  background-color: white;
  background-size: 75%;
}
</style>
