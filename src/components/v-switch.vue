<template>
  <div>
    <div class="is-desktop">
      <component :is="component" v-bind="desktopProps"
        ><slot name="content"
      /></component>
    </div>
    <div class="is-mobile">
      <component :is="component" v-bind="mobileProps"
        ><slot name="content"
      /></component>
    </div>
  </div>
</template>

<script lang="ts">
import Vue, { VNode } from "vue";

export default Vue.extend({
  props: {
    component: {
      type: Function,
      required: true,
    },
    desktopProps: {
      type: Object,
      required: true,
    },
    mobileProps: {
      type: Object,
      required: true,
    },
  },
});
</script>

<style scoped>
@media screen and (min-width: 480px) {
  .is-desktop {
    display: none;
  }
}

@media not screen and (min-width: 480px) {
  .is-mobile {
    display: none;
  }
}
</style>
