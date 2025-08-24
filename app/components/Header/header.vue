<template>
  <div
    class="bg-[#e5e5e5] flex flex-wrap gap-10 justify-center lg:justify-evenly items-center lg:p-4 lg:h-[80vh] p-10"
  >
    <div class="pt-6 lg:pt-0 w-96 sm:w-52 md:w-64 lg:w-[30em] ">
      <p class="text-sm lg:text-lg font-medium uppercase pb-2">
        printing & branding services
      </p>
      <h1 class="font-bold text-gray-800 lg:text-6xl text-4xl">
        The leader in <br />quality custom
      </h1>

      <p class="text-md font-regular text-gray-800 pt-6">
       Greetings from Skywork, the leading source for branding and printing services in Mombasa.  Whether you need digital printing, corporate branding, or bespoke printing, we specialize in a broad range of tailored printing and branding solutions.
      </p>

      <button
        class="bg-white text-gray-800 font-semibold py-4 px-6 rounded-full mt-10 w-44 p-4 cursor-pointer hover:bg-[#5cc6d0] transition duration-300"
      >
        Shop Now
      </button>
    </div>

    <main>
      <div class="relative z-0 w-64 lg:w-96 overflow-hidden">
        <!-- Images wrapper -->
        <div
          class="flex transition-transform duration-700 ease-in-out"
          :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
        >
          <div
            v-for="(image, index) in images"
            :key="index"
            class="w-full flex-shrink-0 flex justify-center items-center"
          >
            <img :src="image" class="w-64 lg:w-96 sm:h-80 md:h-68 lg:h-[400px] object-cover" />
          </div>
        </div>

        <!-- Navigation dots -->
        <div class="absolute bottom-3 left-1/2 -translate-x-1/2 flex gap-2">
          <button
            v-for="(image, index) in images"
            :key="index"
            @click="currentIndex = index"
            :class="[
              'w-3 h-3 rounded-full',
              currentIndex === index ? 'bg-white' : 'bg-gray-400',
            ]"
          ></button>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
const images = ["/images/t-shirt.png", "/images/women.png", "/images/cap.png", "/images/paper.png"];

const currentIndex = ref(0);
let interval;

onMounted(() => {
  interval = setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % images.length;
  }, 3000); // change slide every 3s
});

onUnmounted(() => {
  clearInterval(interval);
});
</script>
