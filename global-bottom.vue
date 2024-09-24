<template>
  <footer
    v-if="$nav.currentLayout !== 'cover'"
    class="absolute bottom-4 left-8 op20"
  >
    {{ $nav.currentPage }} / {{ $nav.total }}
  </footer>
  <footer class="absolute bottom-4 right-8 op20">{{ now }}</footer>
</template>

<script setup lang="ts">
  import { ref } from 'vue'
  const now = ref(new Date().toLocaleString())

  setInterval(() => {
    now.value = new Date().toLocaleString()
  }, 1000)
</script>
