<script setup lang="ts">

import { ref } from 'vue'

const count = ref(10)

function increment() {
  count.value++
}

</script>

<template>
  <v-btn theme="light" @click="increment">Count is: {{ count }}
    <slot></slot>
  </v-btn>
</template>

<style scoped>

</style>
