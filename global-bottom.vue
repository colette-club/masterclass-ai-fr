<template>
  <footer v-if="$slidev.nav.currentLayout !== 'cover'" class="global-footer">
    Renée Costes — 2026
  </footer>
</template>

<style scoped>
.global-footer {
  position: absolute;
  bottom: 0.5rem;
  right: 1rem;
  font-size: 0.7rem;
  letter-spacing: 0.04em;
  opacity: 0.55;
  pointer-events: none;
}
</style>
