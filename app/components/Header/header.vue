<template>
  <div
    class="bg-[#e5e5e5] flex flex-wrap gap-10 justify-center lg:justify-evenly items-center lg:p-4 lg:h-[80vh] p-10"
  >
    <div class="pt-6 lg:pt-0">
      <p class="text-sm lg:text-lg font-medium uppercase pb-2">
        printing & branding services
      </p>
      <h1 class="font-bold text-gray-800 lg:text-6xl text-4xl">
        The leader in <br />quality custom
      </h1>

      <p class="text-md font-medium text-gray-800 pt-6">
        Turn your ideas into premium products that <br />
        leave a lasting impression.
      </p>

      <button
        class="bg-white text-gray-800 font-semibold py-4 px-6 rounded-full mt-10 w-44 p-4 cursor-pointer hover:bg-[#5cc6d0] transition duration-300"
      >
        Shop Now
      </button>
    </div>

    <div class="w-full max-w-sm overflow-hidden">
      <!-- Images wrapper -->
      <div
        class="flex transition-transform duration-700 ease-in-out"
        :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      >
        <div
          v-for="(image, index) in images"
          :key="index"
          class="w-96 flex-shrink-0"
        >
          <img :src="image" class="w-80 object-cover" />
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
  </div>
</template>

<script setup>
const images = ["/images/t-shirt.png", "/images/women.png", "/images/cap.png"];

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
