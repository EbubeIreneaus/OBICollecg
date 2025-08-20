<template>
  <div>
    <div>
      <h2 class="text-5xl text-center font-extrabold font-playfair mb-7">
        What Parents Says
      </h2>
      <div>
        <div class="swiper-container swiper">
          <div class="swiper-wrapper">
            <UContainer as="blockquote"
              class="text-xl  font-semibold text-gray-900 swiper-slide"
              v-for="review in Reviews"
              :key="review.name"
            >
              <icon name="mdi:format-quote-open" size="34" />
              <p class="text-center italic">
                {{ review.content }}
              </p>
              <p class="text-center font-playfair mt-3">{{ review.name }}</p>
            </UContainer>
          </div>
          <div class="swiper-pagination"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Swiper from "swiper";
import { Pagination, Autoplay } from "swiper/modules";

import "swiper/swiper-bundle.css";
import { UContainer } from "#components";
const Reviews = [
  {
    content:
      "The teachers here are truly dedicated and care about each child’s growth. My son has improved so much academically and socially.",
    name: "Mrs. Angela Thompson",
  },
  {
    content:
      "I love how the school focuses on both academics and extracurricular activities. My daughter enjoys going to school every day.",
    name: "Mr. David Kim",
  },
  {
    content:
      "The communication between parents and teachers is excellent. I always know how my child is doing and what’s going on at school.",
    name: "Mrs. Fatima Ali",
  },
  {
    content:
      "This school has created such a safe and welcoming environment. My children feel supported and valued.",
    name: "Mr. James Carter",
  },
  {
    content:
      "The staff genuinely care about the students’ well-being. I’m grateful for the personal attention my son receives.",
    name: "Mrs. Sophia Martinez",
  },
  {
    content:
      "My daughter has grown in confidence since joining. The teachers inspire her to aim high and believe in herself.",
    name: "Mr. Michael O’Connor",
  },
];
const swiperRef = ref<Swiper | null>(null);

onMounted(() => {
  swiperRef.value = new Swiper(".swiper-container", {
    slidesPerView: 1,
    spaceBetween: 20,
    modules: [Pagination, Autoplay],
    autoplay:{
      delay: 5000
    },
    loop: true,
    breakpoints:{
      768:{
        slidesPerView: 2
      }
    },
    pagination: {
      el: '.swiper-pagination',
      bulletActiveClass: 'text-primary',
      bulletClass: 'text-secondary',
      clickable: true,

    }
  });
});
</script>

<style></style>
