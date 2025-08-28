<template>
  <main class="bg-[#f6f7fb] min-h-screen py-10">
    <div class="max-w-[85rem] mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-lg font-bold text-gray-800 md:text-3xl mb-8">
        Video Gallery
      </h2>

      <!-- Grid -->
      <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(video, index) in videos"
          :key="index"
          class="relative group rounded-xl overflow-hidden shadow-md"
        >
          <!-- Video -->
          <video
            ref="videoEls"
            class="w-full h-56 object-cover"
            :src="video.src"
            preload="metadata"
            muted
          ></video>

          <!-- Play button -->
          <button
            @click="togglePlay(index)"
            class="absolute inset-0 flex items-center justify-center bg-black/40 text-white text-4xl opacity-0 group-hover:opacity-100 transition"
          >
            ▶
          </button>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
const videos = [
  {
    src: "/videos/video.mp4",
  },
  {
    src: "/videos/video2.mp4",
  },
  {
    src: "/videos/video3.mp4",
  },
];

const videoEls = ref([]);
// Make sure we capture the video refs
onMounted(() => {
  videoEls.value = document.querySelectorAll("video");
});

const togglePlay = (index) => {
  const video = videoEls.value[index];

  if (video.paused) {
    // Pause all other videos before playing the clicked one
    videoEls.value.forEach((v, i) => {
      if (i !== index) v.pause();
    });
    video.play();
  } else {
    video.pause();
  }
};
</script>
