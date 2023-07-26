<script setup>
import { RouterView } from 'vue-router'

import AppNavar from '@/views/AppNavar.vue'
</script>

<template>
  <AppNavar />

  <main>
    <RouterView v-slot="{ Component }">
      <Transition name="fade">
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
</style>