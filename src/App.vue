<script setup>
import { RouterView } from 'vue-router'

import AppNavar from '@/views/AppNavar.vue'
</script>

<template>
  <header>
    <AppNavar />
  </header>

  <main>
    <RouterView />
  </main>
</template>

