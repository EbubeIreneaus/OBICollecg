<template>
  <div
    class="hero bg-[url('/images/hero-565.webp')] md:bg-[url('/images/hero-768.webp')] lg:bg-[url('/images/hero-1000.webp')]"
  >
    <div class="relative min-h-[400px] h-full z-30 flex items-center text-center lg:text-left">
      <u-container>
        <p class="text-lg font-bold font-arial text-secondary">The Best College In Abuja</p>
        <h1
          class="text-4xl md:text-5xl lg:text-6xl font-extrabold font-playfair mt-2 mb-5 text-white "
        >
          Welcome To <span class="text-primary">OBI COLLEGE</span>
        </h1>
        <div>
          <u-button icon="mdi:phone" label="Contact Us" variant="soft" size="xl" />
        </div>
      </u-container>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style scoped>
.hero {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: black;
  opacity: 0.7;
  z-index: 10;
}
</style>
