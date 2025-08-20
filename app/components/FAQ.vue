<template>
  <div class="mt-25 mb-10">
    <u-container>
      <h2 class="text-5xl font-playfair font-extrabold text-center mb-7">
        Frequently Asked Questions
      </h2>
      <u-card>
        <template #default>
          <u-accordion
            :items="faqs"
            type="multiple"
            :ui="{
              label: 'text-xl font-extrabold font-arial text-slate-50',
              content: 'text-lg font-arial font-semibold text-slate-100',
            }"
          >
          </u-accordion>
        </template>
      </u-card>
    </u-container>
  </div>
</template>

<script lang="ts" setup>
const faqs = [
  {
    question: "What grades does the school offer?",
    answer:
      "Our school offers classes from Kindergarten through Grade 12, with both primary and secondary education programs.",
  },
  {
    question: "How can I apply for admission?",
    answer:
      "You can apply online through our admissions page or visit the school office to collect an application form.",
  },
  {
    question: "What extracurricular activities are available?",
    answer:
      "We offer sports teams, music clubs, debate societies, art workshops, and community service programs.",
  },
  {
    question: "Does the school provide transportation?",
    answer:
      "Yes, we have a school bus service covering several routes across the city. Contact the admin office for schedules and fees.",
  },
  {
    question: "Are meals provided at school?",
    answer:
      "Yes, we have a cafeteria that serves breakfast, lunch, and snacks, with healthy menu options.",
  },
  {
    question: "How can parents communicate with teachers?",
    answer:
      "Parents can reach teachers via the school’s parent portal, email, or by scheduling in-person meetings.",
  },
  {
    question: "What is the school’s policy on technology use?",
    answer:
      "Students are encouraged to use technology for learning purposes only. Personal device use is regulated during school hours.",
  },
].map((x) => ({ label: x.question, content: x.answer }));
</script>

<style></style>
