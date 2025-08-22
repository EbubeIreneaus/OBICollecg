<template>
  <div class="mb-20" id="gallery">
    <div class="overflow-x-hidden mx-5">
      <div class="row1">
        <div class="flex flex-nowrap gap-x-1 track1">
          <!-- Render images twice for seamless looping -->
          <nuxt-img
            :src="`/images/gallery/${img}`"
            alt="school gallery image"
            width="350"
            height="250"
            format="webp"
            densities="x1"
            quality="80"
            v-for="(img, index) in [...imgs1, ...imgs1]"
            :key="'img1-' + index"
            loading="lazy"
          />
        </div>
      </div>

      <div class="row2">
        <div class="flex flex-nowrap gap-x-1 track2">
          <!-- Render images twice for seamless looping -->
          <nuxt-img
            :src="`/images/gallery/${img}`"
            alt="school gallery image"
            width="350"
            height="250"
            format="webp"
            densities="x1"
            quality="80"
            v-for="(img, index) in [...imgs2, ...imgs2]"
            :key="'img2-' + index"
            loading="lazy"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, onUnmounted } from 'vue';

const imgs1 = [
  "01.jpg",
  "02.jpg",
  "03.jpg",
  "04.jpg",
  "05.jpg",
  "06.jpg",
  // Removed duplicates since we handle looping in the template
];
const imgs2 = [
  "07.jpeg",
  "08.jpeg",
  "09.jpeg",
  "10.jpeg",
  "11.jpeg",
  "12.jpeg",
  // Removed duplicates since we handle looping in the template
];

// Set animation properties dynamically
const setAnimationProperties = () => {
  const track1 = document.querySelector('.track1') as HTMLElement | null;
  const track2 = document.querySelector('.track2') as HTMLElement | null;
  if (track1 && track2) {
    const track1Width = track1.scrollWidth / 2; // Divide by 2 since images are duplicated
    const track2Width = track2.scrollWidth / 2; // Divide by 2 since images are duplicated
    const baseDuration = 25; // Base duration in seconds
    const duration1 = (track1Width / 1000) * baseDuration; // Scale duration by track width
    const duration2 = (track2Width / 1000) * baseDuration;

    // Set animation duration
    track1.style.animationDuration = `${duration1}s`;
    track2.style.animationDuration = `${duration2}s`;

    // Set CSS custom property for translation distance
    track1.style.setProperty('--track-width', `-${track1Width}px`);
    track2.style.setProperty('--track-width', `-${track2Width}px`);
  }
};

// Run on mount and window resize
onMounted(() => {
  setAnimationProperties();
  window.addEventListener('resize', setAnimationProperties);
});

onUnmounted(() => {
  window.removeEventListener('resize', setAnimationProperties);
});
</script>

<style scoped>
/* Ensure the container hides overflow */
.row1,
.row2 {
  overflow-x: hidden;
  width: 100%;
}

/* Ensure tracks don't wrap and take up only the necessary space */
.track1,
.track2 {
  display: inline-flex;
  white-space: nowrap;
}

/* Animation for track1 (left scroll) */
.track1 {
  animation: scrollleft var(--animation-duration, 25s) linear infinite;
}

/* Animation for track2 (right scroll) */
.track2 {
  animation: scrollright var(--animation-duration, 25s) linear infinite;
}

/* Pause animation on hover (optional for better UX) */
.track1:hover,
.track2:hover {
  animation-play-state: paused;
}

/* Keyframes using track width */
@keyframes scrollleft {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(var(--track-width)); /* Move by the full track width */
  }
}

@keyframes scrollright {
  0% {
    transform: translateX(var(--track-width)); /* Start from the left */
  }
  100% {
    transform: translateX(0); /* Move to the right */
  }
}
</style>