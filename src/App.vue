<template>
  <div id="app-root">
    <PreloaderSection />
    <RouterView />
    <AppFooter />
    <ScrollTopSection />
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import PreloaderSection from '@/components/sections/PreloaderSection.vue'
import AppFooter from '@/components/sections/AppFooter.vue'
import ScrollTopSection from '@/components/sections/ScrollTopSection.vue'

onMounted(() => {
  if (window.WOW) {
    new window.WOW().init()
  }
})
</script>

<style>
@import '@/assets/landing.css';
</style>
