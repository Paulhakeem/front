<template>
  <section
    class="bg-[#f6f7fb] max-w-[85rem] pt-14 mx-auto px-4 sm:px-6 lg:px-8"
  >
    <div class="grid md:grid-cols-2 gap-4 md:gap-8 xl:gap-20">
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
        <div class="mt-6 space-y-2 text-gray-800">
          <p>
            Phone:
            <a href="tel:+1234567890" class="text-gray-800">+1 234 567 890</a>
          </p>
          <p>
            Email:
            <a href="mailto:" class="text-gray-800">Email </a>
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
