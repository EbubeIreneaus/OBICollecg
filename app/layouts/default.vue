<template>
  <div>
    <header>
      <u-container as="div" class="flex justify-between items-center">
        <nuxt-img
          src="/logo-tr.png"
          width="250"
          height="100"
          alt="logo"
          format="webp"
          class="h-[100px]"
        />
        <div class="items-center gap-x-2 hidden md:flex text-black">
          <div class="border rounded-full px-2 py-1">
            <icon name="mdi:phone" size="40" color="secondary" />
          </div>
          <p class="font-extrabold text-4xl font-arial">08061982520</p>
        </div>
      </u-container>
      <nav
        class="bg-primary justify-between items-center px-10 py-3 hidden lg:flex"
      >
        <ul class="flex gap-x-4 items-center">
          <li v-for="link in navLinks" :key="link.href" class="text-white">
            <a :href="link.href" class="capitalize font-arial font-semibold">
              {{ link.label }}</a
            >
          </li>
        </ul>
        <div class="flex items-center">
          <u-input
            variant="soft"
            size="xl"
            placeholder="search here"
            :ui="{
              root: 'text-neutral border-0 outline-0',
              base: 'rounded-none rounded-l-lg',
            }"
          />
          <u-button
            aria-label="search action"
            icon="mdi:magnify"
            size="xl"
            variant="soft"
            class="rounded-none rounded-r-lg"
            color="neutral"
          />
        </div>
      </nav>
      <div class="bg-primary block lg:hidden">
        <u-container as="div">
          <div class="flex justify-end py-3">
            <u-button
              size="xl"
              variant="soft"
              color="neutral"
              icon="mdi:menu"
              aria-label="toggle menu"
              @click="openNavMd = !openNavMd"
            />
          </div>

          <nav class="nav-md" :class="{ open: openNavMd }">
            <ul>
              <li
                v-for="link in navLinks"
                :key="link.href"
                class="text-neutral font-arial text-lg font-semibold capitalize"
              >
                <a
                  :href="link.href"
                  class="block p-2 hover:!bg-secondary hover:text-black text-center"
                  >{{ link.label }}</a
                >
              </li>
              <li class="flex items-center mx-auto w-fit py-4">
                <u-input
                  variant="soft"
                  size="xl"
                  placeholder="search here"
                  :ui="{
                    root: 'text-neutral border-0 outline-0',
                    base: 'rounded-none rounded-l-lg',
                  }"
                />
                <u-button
                  aria-label="search action"
                  icon="mdi:magnify"
                  size="xl"
                  variant="soft"
                  class="rounded-none rounded-r-lg"
                  color="neutral"
                />
              </li>
            </ul>
          </nav>
        </u-container>
      </div>
    </header>
    <slot />
    <footer class="bg-primary text-white px-5 md:px-7 lg:px-10">
      <div>
        <div class="grid grid-cols-3 gap-y-10 gap-x-5 p-5">
          <div class="col-span-3 lg:col-span-1">
            <nuxt-img
              src="/logo-tr.png"
              format="webp"
              width="250"
              height="100"
              quality="80"
              class="h-[100px]"
              alt="logo"
             
            />
          </div>

          <div class="col-span-3 md:col-span-1">
            <div class="text-xl font-playfair font-extabold mb-3">Links</div>
            <ul>
              <li
                v-for="link in navLinks"
                :key="link.href"
                class="flex items-center gap-x-1 font-arial text-lg font-bold hover:scale-110 transition-all linear duration-300"
              >
                <icon name="mdi:chevron-right" />
                <a :href="link.href" class="capitalize">{{ link.label }}</a>
              </li>
            </ul>
          </div>

          <div class="col-span-3 md:col-span-1">
            <div class="text-xl font-playfair font-extabold mb-3">Address</div>
            <ul>
              <li
                class="flex items-center gap-x-2 font-arial font-bold text-lg mb-3"
              >
                <icon name="mdi:phone-classic" size="20" />
                <span>08061982520</span>
              </li>
              <li
                class="flex items-center gap-x-2 font-arial font-bold text-lg mb-3"
              >
                <icon name="mdi:email" size="20" />
                <span>guidance@obicollege.com</span>
              </li>
              <li
                class="flex items-center gap-x-2 font-arial font-bold text-lg mb-3"
              >
                <icon name="mdi:map-marker" size="20" />
                <span>
                  Beside Top up hotel, along Bwari - Garam road <br />
                  Azhi Bisa Niger State
                </span>
              </li>
            </ul>
          </div>
        </div>

        <div class="h-0.5 bg-slate-50"></div>

        <div class="flex justify-between items-center flex-wrap px-5 py-2">
          <div class="text-lg font-extrabold font-arial">
            &copy;{{ new Date().getFullYear() }} OBI COLLEGE
          </div>
          <div class="flex item-center gap-x-2">
            <a href="#" aria-label="facebook">
              <icon name="mdi:facebook" size="30" />
            </a>
            <a href="#" aria-label="twitter">
              <icon name="mdi:twitter-box" size="30" />
            </a>
            <a href="#" aria-label="linkedin">
              <icon name="mdi:linkedin" size="30" />
            </a>
            <a href="#" aria-label="instagram">
              <icon name="mdi:instagram" size="30" />
            </a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script lang="ts" setup>
const navLinks = [
  { label: "home", href: "/" },
  { label: "about us", href: "/about" },
  { label: "events", href: "#event" },
  { label: "Gallery", href: "#gallery" },
  { label: "support", href: "support" },
];
const openNavMd = ref(false);
</script>

<style scoped>
.nav-md {
  max-height: 0;
  overflow: hidden;
  opacity: 0;
  transition: all 0.3s linear;
}

.nav-md.open {
  max-height: 1000px;
  opacity: 1;
}
</style>
