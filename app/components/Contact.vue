<template>
  <div class="py-20 bg-slate-100">
    <UContainer class="grid lg:grid-cols-2 gap-5" id="support">
      <div>
        <h2 class="text-5xl font-extrabold font-playfair">Reach Out To Us</h2>
        <p class="text-lg font-medium mb-4 mt-1">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ullam,
          aliquam.
        </p>
        <div>
          <div class="flex items-center gap-x-3 mb-5">
            <div
              class="ring rounded-full ring-primary flex items-center justify-center size-[50px]"
            >
              <icon name="mdi:email-newsletter" size="25" />
            </div>
            <div class="">
              <span class="text-black/50 font-semibold block leading-tight"
                >Email</span
              >
              <a href="#" class="text-lg font-semibold block"
                >guidance@obicollege.com</a
              >
            </div>
          </div>

          <div class="flex items-center gap-x-3 mb-5">
            <div
              class="ring rounded-full ring-primary flex items-center justify-center size-[50px]"
            >
              <icon name="mdi:phone" size="25" />
            </div>
            <div class="">
              <span class="text-black/50 font-semibold block leading-tight"
                >Call Us</span
              >
              <a
                href="#"
                class="text-lg font-semibold block"
                aria-label="call us on 08061982520"
                >08061982520</a
              >
            </div>
          </div>

          <div class="flex items-center gap-x-3 mb-5">
            <div
              class="ring rounded-full ring-primary flex items-center justify-center size-[50px]"
            >
              <icon name="mdi:map-marker" size="25" />
            </div>
            <div class="">
              <span class="text-black/50 font-semibold block leading-tight"
                >Grab a cup of coffee</span
              >
              <p class="font-semibold text-lg">
                Beside Top up hotel, along Bwari - Garam road <br />
                Azhi Bisa Niger State
              </p>
            </div>
          </div>

          <div>
            <div class="text-2xl font-bold font-arial mb-3">Socials</div>
            <div class="flex gap-x-3 items-center">
              <u-button
                icon="mdi:facebook"
                aria-label="facebook"
                size="xl"
                vriant="soft"
                color="neutral"
              />
              <u-button
                icon="mdi:twitter"
                aria-label="twitter"
                size="xl"
                vriant="soft"
                color="neutral"
              />
              <u-button
                icon="mdi:instagram"
                aria-label="instagram"
                size="xl"
                vriant="soft"
                color="neutral"
              />
              <u-button
                icon="mdi:linkedin"
                aria-label="linkedin"
                size="xl"
                vriant="soft"
                color="neutral"
              />
            </div>
          </div>
        </div>
      </div>

      <div>
        <u-card>
          <template #default>
            <form @submit.prevent="console.log('message sent')">
              <UFormField label="Fullname" required class="mb-3.5">
                <u-input variant="soft" class="w-full" size="lg"  />
              </UFormField>
              <UFormField label="Email" required class="mb-3.5">
                <u-input variant="soft"  class="w-full" size="lg" />
              </UFormField>
              <UFormField label="Subject" required class="mb-3.5">
                <u-input variant="soft"  class="w-full" size="lg" />
              </UFormField>
              <UFormField label="Message" required class="mb-5">
                <u-textarea variant="soft" :rows="3" class="w-full" size="lg" />
              </UFormField>
              <u-button label="Send" icon="mdi:send" variant="soft" />
            </form>
          </template>
        </u-card>
      </div>
    </UContainer>
  </div>
</template>

<script lang="ts" setup></script>

<style></style>
