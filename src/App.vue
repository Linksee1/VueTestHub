<script setup lang="ts">
import { RouterView } from 'vue-router'
import FooterBlock from '@/components/FooterBlock.vue'
import HeaderBlock from '@/components/HeaderBlock.vue'
</script>

<template>
  <v-app>
    <HeaderBlock/>
      <v-main>
        <RouterView />
      </v-main>
    <FooterBlock/>
  </v-app>
</template>

<style scoped>
</style>
