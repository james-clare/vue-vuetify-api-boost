<template>
  <div :max-width="1024" class="centered">
    <v-responsive :aspect-ratio="40 / 31">
      <div class="video">
        <v-responsive :aspect-ratio="16 / 9">
          <vue-vimeo-player ref="player" video-id="492614777" />
        </v-responsive>
      </div>

      <div class="options">
        <v-responsive :aspect-ratio="5 / 1">
          Options
        </v-responsive>
      </div>
    </v-responsive>
  </div>
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

<style>
.centered {
  position: fixed;
  top: 50%;
  left: 50%;
  /* bring your own prefixes */
  transform: translate(-50%, calc(-50%));
  min-width: 56.2%;
  background: lightblue !important;
}
.video {
  background: green;
}
.options {
  background: orange;
}
</style>
