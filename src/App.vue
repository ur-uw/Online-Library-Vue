<template>
  <NavBar v-if="showNavBar" />
  <router-view />
  <!-- <h1>{{ this.route.name }}</h1> -->
</template>
<script>
import { computed } from "vue";

import NavBar from "./components/NavBar";
import router from "./router";
export default {
  name: "App",
  components: {
    NavBar,
  },
  setup() {
    var showNavBar = computed(
      () =>
        router.currentRoute.value.path != "/login" &&
        router.currentRoute.value.path != "/register"
    );
    return { showNavBar };
  },
};
</script>

<style lang="scss">
@import "./sass/app.scss";
</style>
