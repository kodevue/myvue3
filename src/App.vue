<script setup>
import { RouterView } from 'vue-router'

import AppNavar from '@/views/AppNavar.vue'
</script>

<template>
  <AppNavar />

  <main>
    <RouterView v-slot="{ Component }">
      <Transition>
        <component :is="Component" />
      </Transition>
    </RouterView>
  </main>
</template>

<style>
/* we will explain what these classes do next! */
.v-enter-active,
.v-leave-active {
  transition: opacity 0.7s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>