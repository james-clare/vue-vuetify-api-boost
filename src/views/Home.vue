<template>
  <v-main>
    <transition name="fade">
      <Welcome v-if="!started" @start="started = true"></Welcome>
    </transition>
    <transition name="fade">
      <VideoHolder v-if="started"></VideoHolder>
    </transition>
    <!-- <v-img src="../assets/img/newspaper-bg.jpg" contain max-width="100vw" /> -->
  </v-main>
</template>

<script>
export default {
  name: "Home",
  components: {
    Welcome: () => import("../components/Welcome"),
    VideoHolder: () => import("../components/VideoHolder")
  },
  data() {
    return {
      started: true
    };
  },
  head: {
    title: {
      inner: "Home"
    },
    meta: [
      {
        name: "home",
        id: "home",
        content: "Home's very real."
      }
    ]
  }
};
</script>
<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

main {
  height: 100vh;
  background: url(../assets/img/newspaper-bg.jpg) no-repeat 0% 0%/100%;
  background-position: center center;
}
</style>
