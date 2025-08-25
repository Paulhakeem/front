<template>
  <div class="bg-[#f6f7fb] lg:px-10">
    <div
      class="flex flex-wrap justify-evenly place-content-center items-center space-y-12 p-10"
    >
      <div
        v-for="(item, index) in services"
        :key="index"
        class="bg-[#ffffff] p-4 size-70 rounded-md"
      >
        <h4 class="text-md font-semibold text-gray-800 uppercase">
          {{ item.title }}
        </h4>
        <div>
          <img :src="item.src" alt="" class="w-64 mt-2">
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  { title: "Business Cards", src: "/images/businesscard.jpg" },
  { title: "Marketing Materials", src: "/images/bronchure.jpg" },
  { title: "Signs & Posters", src: "/images/3.png" },
  { title: "T-shirts & Bags Printing", src: "/images/t-shirt.png" },
  { title: "Design Services", src: "/images/5.png" },
  { title: "Invitation & Stationery", src: "/images/6.png" },
  { title: "Labels & Stickers", src: "/images/7.png" },
];
</script>
