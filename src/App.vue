<template>
  <v-switch>
    <template v-slot:desktop>
      <v-text color="red" bold />
    </template>
    <template v-slot:mobile>
      <v-text color="blue" />
    </template>
    <template v-slot:content> content </template>
  </v-switch>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import VSwitch from "./components/v-switch.vue";
import VText from "./components/v-text.vue";

export default defineComponent({
  name: "App",
  components: {
    VSwitch,
    VText,
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
