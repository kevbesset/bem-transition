<script>
import { h, Transition } from "vue";

export default {
  name: "BemTransition",
  props: {
    name: { type: String },
  },
  render() {
    return h(
      Transition,
      {
        ...this.$attrs,
        name: this.name ? `${this.name}-` : this.name,
      },
      this.$slots
    );
  },
};
</script>
