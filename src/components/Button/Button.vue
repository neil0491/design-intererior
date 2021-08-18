<template>
  <button class="btn" :class="primary ? 'btn-primaty' : 'btn-secondary'">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
      default: "Get Started",
    },
    primary: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
}
</script>

<style scoped lang="scss">
.btn {
  font-size: 1.5rem;
}
</style>
