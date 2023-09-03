<template>
  <v-app-bar flat>
    <v-app-bar-title> v-app-bar-title </v-app-bar-title>
    <v-tabs>
      <v-tab v-for="col in menuItem" :to=col[1] exact> {{ col[0] }} </v-tab>
    </v-tabs>
  </v-app-bar>
</template>

<script setup>
const menuItem = [
  ['view00', '/'],
  ['view01', '/view01'],
  ['view02', '/view02'],
  ['view03', '/view03'],
  ['about', '/about'],
];
</script>
