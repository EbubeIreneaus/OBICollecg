<template>
  <div class="mb-20">
    <u-container id="event">
      <h2 class="text-5xl font-extrabold font-playfair mb-7 text-center">
        Upcoming Events
      </h2>
      <div class="mb-3" v-for="ev in events" :key="ev.id">
        <u-card
          variant="soft"
          :ui="{ root: 'bg-slate-200 rounded-2xl ring-0' }"
        >
          <template #default>
            <div class="flex gap-x-3">
              <div
                class="h-full flex flex-col gap-y-1.5 justify-center bg-slate-950 text-slate-200 p-3 rounded-xl"
              >
                <p class="font-mono text-lg font-semibold text-center">
                  {{ ev.date }}
                </p>
                <div class="text-2xl font-extrabold text-center">
                  {{ ev.time }}
                </div>
              </div>
              <div class="flex-grow">
                <div class="font-bold text-2xl  mb-1">
                  {{ ev.title }}
                </div>
                <p class="text-lg font-arial">
                  {{ ev.desc }}
                </p>
              </div>
            </div>
          </template>
        </u-card>
      </div>
    </u-container>
  </div>
</template>

<script lang="ts" setup>
const events = [
  {
    id: 1,
    date: "Sep 05",
    time: "08:00",
    title: "School Resumption",
    desc: "The new academic session begins. All students are expected to resume with necessary materials and be prepared for orientation programs.",
  },
  {
    id: 2,
    date: "Sep 12",
    time: "10:00",
    title: "Orientation Day",
    desc: "A special program to welcome new students and parents. Staff will introduce school policies, academic expectations, and extracurricular activities.",
  },
  {
    id: 3,
    date: "Oct 01",
    time: "09:30",
    title: "Independence Day Celebration",
    desc: "Students and staff will gather to celebrate Independence Day with cultural performances, parades, and special guest speakers.",
  },
  {
    id: 4,
    date: "Oct 15",
    time: "11:00",
    title: "Midterm Examination",
    desc: "The first term midterm examinations commence. Students should check their schedules and prepare adequately for all subjects.",
  },
  {
    id: 5,
    date: "Nov 20",
    time: "14:00",
    title: "Inter-House Sports Competition",
    desc: "Annual sports competition where students from different houses compete in athletics, football, and other exciting events.",
  },
];
</script>

<style></style>
