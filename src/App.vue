<template>
  <v-switch
    :component="VText"
    :desktopProps="desktopProps"
    :mobileProps="mobileProps"
  >
    <template v-slot:content> content </template>
  </v-switch>
</template>

<script lang="ts">
import Vue from "vue";
import VSwitch from "./components/v-switch.vue";
import VText from "./components/v-text.vue";

export default Vue.extend({
  name: "App",
  components: {
    VSwitch,
    VText,
  },
  computed: {
    VText() {
      return VText;
    },
    desktopProps() {
      return {
        bold: true,
        color: "blue",
      };
    },
    mobileProps() {
      return {
        bold: false,
        color: "red",
      };
    },
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
