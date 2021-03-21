<template>
  <v-app>
    <!-- <v-container fluid> -->
    <!-- 
        The key refreshes component in some wierd cases. 
        You may or may not want this 
      -->
    <router-view :key="$route.fullPath" />
    <!-- </v-container> -->
  </v-app>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
@import "./assets/css/main.css";
</style>
