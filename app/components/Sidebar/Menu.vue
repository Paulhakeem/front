<template>
  <nav class="bg-white flex items-center justify-between p-4">
    <!-- Left side menu -->
    <ul class="flex space-x-6">
      <li v-for="(item, index) in menu" :key="index">
        <a
          :href="item.path"
          class="text-gray-800 hover:border-b hover:border-b-[#d8f3f4] text-sm font-medium tracking-wide uppercase"
        >
          {{ item.name }}
        </a>
      </li>
    </ul>

    <!-- Center icon -->
    <div class="flex justify-center flex-1">
      <Icon name="ph:dev-to-logo-fill" class="text-gray-700 text-6xl" />
    </div>

    <!-- Right side (placeholder for profile/login/etc) -->
    <div class="flex justify-end items-center">
      <div>
        <input
          type="text"
          placeholder="Search for product"
          class=" px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-[#d8f3f4]"
        />
      </div>
    </div>
  </nav>
</template>

<script setup>
const menu = ref([
  { name: "Home", path: "/" },
  { name: "About", path: "/about" },
  { name: "Services", path: "/services" },
  { name: "Contact", path: "/contact" },
]);
</script>
