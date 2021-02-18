<script lang="ts">
import { defineComponent, h } from "vue";
export default defineComponent({
  setup(_, { slots }) {
    if (!slots.content) throw new Error("missing content");
    if (!slots.A) throw new Error("missing A");

    console.log(slots.content());
    console.log(slots.A()[0]);

    return () => h("div", {}, [slots.A!({ poyo: 10 })]);
  },
});
</script>
