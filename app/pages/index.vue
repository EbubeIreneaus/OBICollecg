<template>
  <main>
    <hero-comp />
    <why-us />
    <AboutUs />
    <Gallery/>
    <EventSection />
    <Anthem />
    <ParentReviews />
    <f-a-q />
    <contact />
  </main>
</template>

<script lang="ts" setup>
const title = 'OBI International College Abuja'
const desc='We Are No.1 Standard Internation College, Kubwa Abuja, Giving Student The Best Legacy'
useHead({
  link: [
    {rel:'canonical', href: 'https://obi-college.vercel.app'},
    {rel: 'icon', href: '', type: 'image/png'}
  ],
  htmlAttrs: {
    lang: 'en-US'
  },
})
useSeoMeta({
  title: title,
  ogTitle: title,
  twitterTitle: title,
  description: desc,
  ogDescription:desc,
  twitterDescription: desc,
  ogImage: 'https://obi-college.vercel.app/logo.png',
  twitterImage: 'https://obi-college.vercel.app/logo.png',
  twitterCard: 'summary',
  ogUrl: 'https://obi-college.vercel.app',
  ogType: 'website',
  ogSiteName: title
})

</script>

<style>

</style>