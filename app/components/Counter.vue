<template>
  <div class="grid md:grid-cols-2 gap-3 mt-5">
    <u-card :ui="{ root: 'bg-amber-500 ring-0' }">
      <CountUp

        :endVal="100"
        class="text-2xl font-arial font-extrabold text-center"
      />
      <p class="text-xl font-playfair font-bold text-center mt-3">
        Skilled Teachers
      </p>
    </u-card>
    <u-card variant="soft" :ui="{ root: ' ring-0' }">
      <count-up
        :end-val="200"
        :options="countOptions"
        class="text-2xl font-arial font-extrabold text-center"
      />
      <p class="text-xl font-playfair font-bold text-center mt-3">
        Equiped Classroom
      </p>
    </u-card>
    <u-card variant="soft" :ui="{ root: 'bg-primary ring-0' }">
      <count-up
        :end-val="30000"
        :options="countOptions"
        class="text-2xl font-arial font-extrabold text-center"
      />
      <p class="text-xl font-playfair font-bold text-center mt-3">
        Graduated Student
      </p>
    </u-card>
    <u-card variant="soft" :ui="{ root: 'bg-green-500 ring-0' }">
      <count-up
        :end-val="500"
        :options="countOptions"
        class="text-2xl font-arial font-extrabold text-center"
      />
      <p class="text-xl font-playfair font-bold text-center mt-3">
        Online Course
      </p>
    </u-card>
  </div>
</template>

<script setup>
const countOptions = {
  suffix: "+",
  enableScrollSpy: true,
  scrollSpyOnce: true,
};
</script>

<style></style>
