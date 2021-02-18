<template>
  <v-switch>
    <template v-slot:desktop>
      <red bold><slot></slot></red>
    </template>
    <template v-slot:mobile>
      <blue><slot></slot></blue>
    </template>
    <template v-slot:content> content </template>
  </v-switch>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import VSwitch from "./components/v-switch.vue";
import red from "./components/red.vue";
import blue from "./components/blue.vue";

export default defineComponent({
  name: "App",
  components: {
    VSwitch,
    red,
    blue,
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
