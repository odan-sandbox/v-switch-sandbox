<template>
  <div :class="{ bold, red, blue }">
    <slot />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export type Props = {
  bold: boolean;
  color: string;
};
export default defineComponent({
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
  setup({ bold, color }) {
    return { bold, red: color === "red", blue: color === "blue" };
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
