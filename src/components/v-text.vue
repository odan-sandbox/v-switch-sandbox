<template>
  <div :class="{ bold, red, blue }">
    <slot />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export type Props = {
  bold: boolean;
  color: string;
};
export default Vue.extend({
  props: {
    bold: {
      type: Boolean,
      required: true,
    },
    color: {
      type: String,
      required: true,
    },
  },
  computed: {
    red(): boolean {
      return this.color === "red";
    },
    blue(): boolean {
      return this.color === "blue";
    },
  },
});
</script>

<style scoped>
.red {
  color: red;
}
.blue {
  color: blue;
}
.bold {
  font-weight: 700;
}
</style>
