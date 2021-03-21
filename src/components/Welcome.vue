<template>
  <!-- <v-btn elevation="2" plain @click="$emit('start')">Start Experience</v-btn> -->
  <vue-vimeo-player></vue-vimeo-player>
</template>

<script>
import { vueVimeoPlayer } from "vue-vimeo-player";
export default {
  data: function() {
    return {};
  },
  components: { vueVimeoPlayer }
};
</script>
