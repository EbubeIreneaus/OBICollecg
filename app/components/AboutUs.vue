<template>
  <u-container class="mb-20 py-20">
    <div class="grid lg:grid-cols-2 gap-y-5 items-center mb-10">
      <div>
        <nuxt-img
          src="/images/about-image.jpg"
          format="webp"
          alt="primary school student in a classroom and a female teacher"
          width="500"
          height="300"
          class="rounded-lg mx-auto shadow"
        />
      </div>
      <div>
        <h2 class="text-xl font-arial text-primary font-extrabold">ABOUT US</h2>
        <h3 class="text-4xl font-extrabold font-playfair my-3">
          First choice for your children eduction Abuja
        </h3>
        <p class="text-xl font-medium font-arial">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ad modi
          dicta aliquam voluptatum qui omnis porro, minima vitae aperiam
          assumenda doloremque quos tempore distinctio aliquid inventore,
          facilis iure reprehenderit dolor illo enim eveniet? Voluptatibus amet
          facere delectus nulla consectetur voluptate nisi nam consequatur,
          repellat magni dolore ratione reprehenderit sapiente accusamus.
        </p>
        <ClientOnly>
          <Counter />
        </ClientOnly>
      </div>
    </div>

    <div class="grid md:grid-cols-2 gap-x-3 gap-y-5">
      <u-card :ui="{ root: 'bg-slate-50 ring-0 shadow' }">
        <h2 class="text-2xl font-bold font-playfair mb-3">Mission</h2>
        <p class="text-lg">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
          obcaecati excepturi tempore, maiores labore alias. Nulla dolorem
          deserunt vero, ipsam incidunt ea modi libero corrupti sequi quas
          tempora illo minus.
        </p>
      </u-card>
      <u-card :ui="{ root: 'bg-slate-50 ring-0 shadow' }">
        <h2 class="text-2xl font-bold font-playfair mb-3">Vison</h2>
        <p class="text-lg">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
          obcaecati excepturi tempore, maiores labore alias. Nulla dolorem
          deserunt vero, ipsam incidunt ea modi libero corrupti sequi quas
          tempora illo minus.
        </p>
      </u-card>
    </div>
  </u-container>
</template>

<script setup lang="ts">

</script>

<style></style>
