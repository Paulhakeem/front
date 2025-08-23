<template>
  <div class="bg-[#f6f7fb]">
    <!-- Hero -->
    <div class="max-w-[85rem] mx-auto px-4 sm:px-6 lg:px-8 ">
      <!-- Grid -->
      <div class="grid md:grid-cols-2 gap-4 pt-20 p-2 md:gap-8 xl:gap-20 md:items-center">
        <div class="ms-4">
          <img
            class="w-full rounded-md"
            src="/images/printer.jpg"
            alt="printing machine"
          />
        </div>
        <!-- End Col -->
        <div>
          <h1 class="block text-2xl font-bold text-gray-800 lg:text-4xl">
            About <span class="text-[#5cc6d0]">Us</span> 
          </h1>
          <p class="mt-3 text-md text-gray-800 dark:text-neutral-400 lg:text-lg">
            We are a leading printing company dedicated to providing high-quality
            printing solutions for businesses and individuals. With years of
            experience in the industry, we pride ourselves on our commitment to
            excellence, innovation, and customer satisfaction.  
          </p>
          <p class="mt-3 text-md text-gray-800 dark:text-neutral-400 lg:text-lg">
            Our state-of-the-art printing technology and skilled team ensure that
            every project is executed with precision and care. From business cards
            and brochures to large-format prints and custom designs, we offer a
            wide range of services to meet your unique needs.
          </p>

          <button>
            <NuxtLink
              to="/"
              class="inline-block px-5 py-3 mt-6 text-sm font-medium text-[#31b6bb] rounded-lg border-2 border-[#31b6bb] transition"
            >
              Read More
            </NuxtLink>
          </button>
        </div>
        <!-- End Col -->
      </div>
      <!-- End Grid -->
    </div>
    <!-- End Hero -->
  </div>
</template>

<script setup></script>
