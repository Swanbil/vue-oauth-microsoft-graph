<template>
  <base-button
    :disabled="isPending"
    :color="color"
    :onClick="handleClick"
  >
    <div v-if="isPending" class="spinner-border" role="status">
    </div>
    <slot />
  </base-button>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "AsyncButton",
  components: { BaseButton },
  inheritAttrs: false,

  props: {
    color: {
      type: String,
      default: "primary",
    },
  },

  data() {
    return {
      isPending: false,
    };
  },

  methods: {
    handleClick() {
      console.log(this.isPending);
      const originalOnClick = /** @type {() => Promise<void>} */ (
        this.$attrs.onClick
      );
      this.isPending = true;
      originalOnClick().finally(() => {
        this.isPending = false;
      });
    },
  },
};
</script>