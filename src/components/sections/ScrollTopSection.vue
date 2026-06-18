<template>
  <a
    href="#"
    class="scroll-top"
    :style="{ display: showScroll ? 'block' : 'none' }"
    @click.prevent="scrollToTop"
  >
    <i class="lni lni-arrow-up"></i>
  </a>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const showScroll = ref(false)

function handleScroll() {
  showScroll.value = document.body.scrollTop > 50 || document.documentElement.scrollTop > 50
}

function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
