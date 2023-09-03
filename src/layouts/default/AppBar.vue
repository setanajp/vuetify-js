<template>
  <v-app-bar flat>
    <v-app-bar-nav-icon v-if="$vuetify.display.xs" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    <v-app-bar-title> v-app-bar-title </v-app-bar-title>
    <v-tabs v-if="$vuetify.display.smAndUp">
      <v-tab v-for="col in menuItem" :to=col[1] exact> {{ col[0] }} </v-tab>
    </v-tabs>
  </v-app-bar>

  <v-navigation-drawer v-if="$vuetify.display.xs" v-model="drawer">
    <v-list-item v-for="col in menuItem" @click.stop="drawer = false" :to=col[1] exact> {{ col[0] }} </v-list-item>
  </v-navigation-drawer>
</template>

<script setup>
import { ref } from "vue";

const drawer = ref(false);
const menuItem = [
  ['view00', '/'],
  ['view01', '/view01'],
  ['view02', '/view02'],
  ['view03', '/view03'],
  ['about', '/about'],
];
</script>
