<template>
  <div class="bg-[#f6f7fb]">
    <div class="flex flex-wrap justify-evenly place-content-center items-center gap-10 p-10">
      <div v-for="(item, index) in services" :key="index"  class="bg-[#ffffff] p-4 size-70 rounded-md">
        <h4 class="text-lg font-semibold text-gray-800 uppercase">{{ item.title }}</h4>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = ([
  { title: 'Business Cards' },
  { title: 'Marketing Materials' },
  { title: 'Signs & Posters' },
  { title: 'Clothing & Bags' },
  { title: 'Design Services' },
  { title: 'Invitation & Stationery' },
  { title: 'Labels & Stickers' },
  { title: 'Photo Gifts & Calendars' }
])

</script>
