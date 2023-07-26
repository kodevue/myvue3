<script setup>
import { RouterView } from 'vue-router'

import AppNavar from '@/views/AppNavar.vue'
</script>

<template>
  <AppNavar />

  <main>
    <RouterView v-slot="{ Component }">
      <Transition name="page-slide">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </main>
</template>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: 500ms ease all;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.page-slide-enter-active,
.page-slide-leave-active {
  transition: 800ms ease all;
}

.page-slide-enter-from,
.page-slide-leave-to {
  opacity: 0;
  transform: translateY(60px);
}
</style>