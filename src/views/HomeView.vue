<script setup lang="ts">
import ButtonCount from '@/components/ButtonCount.vue'
</script>

<template>
  <main>
      <v-container class="bg-surface-variant">
        <v-row no-gutters>
          <v-col
            v-for="n in 3"
            :key="n"
            cols="12"
            sm="4"
          >
            <v-sheet class="ma-2 pa-2">
              <ButtonCount>{{ n }}</ButtonCount>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
  </main>
</template>
