<script>
import { h, TransitionGroup } from "vue";

export default {
  name: "BemTransitionGroup",
  props: {
    name: { type: String },
  },
  render() {
    return h(
      TransitionGroup,
      {
        ...this.$attrs,
        name: this.name ? `${this.name}-` : this.name,
      },
      this.$slots
    );
  },
};
</script>
