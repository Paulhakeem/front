<template>
  <section
    class="bg-[#f6f7fb]"
  >
    <div class="grid md:grid-cols-2 gap-4 px-6 pt-15 md:gap-8 xl:gap-20 lg:pt-20">
      <div class="pb-4">
        <h2 class="text-2xl font-bold text-[#5cc6d0]">Contact Us</h2>
        <p class="mt-3 text-md text-gray-800 lg:text-md">
          Place your order, ask for a quote, or just say hello! Our team is here
          to assist you with all your printing and branding needs. Fill out the
          form below and we'll get back to you as soon as possible.
        </p>
        <p class="mt-3 text-md text-gray-800 lg:text-md">
          Add your printing design file if you have any so that we can provide
          you with an accurate quote.
        </p>
        <div class="mt-6 space-y-4 text-gray-800">
          <p class="flex items-center">
            <Icon
              name="mingcute:whatsapp-fill"
              class="text-2xl mr-1 text-[#5cc6d0]"
            />
            <a href="tel:+254719283858" class="text-gray-800">+254 719 283 858</a>
          </p>
          <p class="flex items-center">
            <Icon
              name="ic:round-email"
              class="text-2xl mr-1 text-[#5cc6d0]"
            />
            <a href="mailto:skywork021@gmail.com" class="text-gray-800">skywork021@gmail.com </a>
          </p>
          <p class="flex items-center">
            <Icon
              name="ic:round-location-on"
              class="text-2xl mr-1 text-[#5cc6d0]"
            />
            <span class="text-gray-800"
              >123 Printing St, Print City, PC 12345</span
            >
          </p>
        </div>
      </div>
      <form class="flex flex-col gap-4">
        <input
          type="text"
          placeholder="Your Name"
          class="p-2 border border-gray-300 rounded"
        />
        <input
          type="email"
          placeholder="Your Email"
          class="p-2 border border-gray-300 rounded"
        />
        <input type="file" class="p-2 border border-gray-300 rounded" />
        <textarea
          placeholder="Your Message"
          class="p-2 border border-gray-300 rounded h-32"
        ></textarea>
        <button type="submit" class="bg-[#5cc6d0] text-white p-2 rounded">
          Send Message
        </button>
      </form>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped></style>
