<script setup lang="ts">
import { ref } from 'vue'

const drawer = ref(false)
const items = ref([
  {
    title: 'Home',
    href: '/'
  },
  {
    title: 'Grid',
    href: '/grid'
  },
  {
    title: 'Tables',
    href: '/tables'
  },
  {
    title: 'Carousel',
    href: '/car'
  },
  {
    title: 'Form',
    href: '/form'
  }
])
</script>

<template>
  <v-app-bar>
    <v-container>
      <v-row>
        <v-col class="flex-grow-0 pa-0 align-content-center">
          <v-btn @click.stop="drawer = !drawer" class="pa-0">
            <div class="menu_btn d-flex	flex-column justify-space-evenly">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </v-btn>
        </v-col>
        <v-col class="align-content-center">
          <v-app-bar-title>Application Bar</v-app-bar-title>
        </v-col>
      </v-row>

    </v-container>
  </v-app-bar>
  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'bottom' : undefined"
    temporary
  >
    <v-list>
      <v-list-item v-for="i in items" :key="i.title" :to="i.href" link>{{i.title}}</v-list-item>

    </v-list>
  </v-navigation-drawer>
</template>

<style scoped lang="scss">
.menu {
  &_btn {
    height: 27px;
    width: 27px;

    & span {
      width: 100%;
      background-color: white;
      height: 2px;
    }
  }
}
</style>
