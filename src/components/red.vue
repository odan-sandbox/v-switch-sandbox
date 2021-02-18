<template>
  <div class="red" :class="{ bold }">
    <slot />
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
export type Props = {
  bold: boolean;
};
export default defineComponent({
  props: {
    bold: {
      type: Boolean,
      required: true,
    },
  },
  setup({ bold }) {
    return { bold };
  },
});
</script>

<style scoped>
.red {
  color: red;
}
.bold {
  font-weight: 700;
}
</style>
