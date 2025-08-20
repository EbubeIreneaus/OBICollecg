<template>
  <div class="px-5 mb-12 my-3">
    <div class="grid md:grid-cols-3 gap-x-5 gap-y-5">
      <u-card
        class=""
        :ui="{
          root: 'bg-white ring-0 shadow-sm shadow-primary',
        }"
      >
        <div>
          <nuxt-img
            src="/images/icons/education.png"
            format="webp"
            width="50"
            height="50"
            alt="enviromental icon"
          />
          <p class="text-xl font-playfair font-extrabold my-2">
            Quality Education
          </p>
          <p class="text-base font-arial">
            Our experienced teachers use modern teaching methods to ensure every
            student receives a well-rounded and engaging education.
          </p>
        </div>
      </u-card>
      <u-card
        class=""
        :ui="{
          root: 'bg-white ring-0 shadow-md shadow-primary',
        }"
      >
        <div>
          <nuxt-img
            src="/images/icons/enviroment.png"
            format="webp"
            width="50"
            height="50"
            alt="enviromental icon"
          />
          <p class="text-xl font-playfair font-extrabold my-2">
            Condusive Enviroment
          </p>
          <p class="text-base font-arial">
            We prioritize the safety, well-being, and personal growth of every
            student, creating a positive atmosphere for learning.
          </p>
        </div>
      </u-card>
      <u-card
        class=""
        :ui="{
          root: 'bg-white ring-0 shadow-sm shadow-primary',
        }"
      >
        <div>
          <nuxt-img
            src="/images/icons/opportunity.png"
            format="webp"
            width="50"
            height="50"
            alt="opportunities icon"
          />
          <p class="text-xl font-playfair font-extrabold my-2">
            UnEnding Opprtunities
          </p>
          <p class="text-base font-arial">
            From sports and arts to leadership programs, our extracurricular
            activities help students discover their talents and passions.
          </p>
        </div>
      </u-card>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style></style>
