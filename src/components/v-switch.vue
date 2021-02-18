<template>
  <div>
    <div class="is-desktop">
      <component :is="desktop"><slot name="content"></slot></component>
    </div>
    <div class="is-mobile">
      <component :is="mobile"><slot name="content"></slot></component>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup(_, { slots }) {
    return { desktop: slots.desktop!()[0], mobile: slots.mobile!()[0] };
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
