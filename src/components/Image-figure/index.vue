<template>
  <div class="image-container">
    <div
      :class="[
        {
          round: round,
          'round-top': top,
          'round-bottom': bottom,
          'round-left': left,
          'round-right': right,
          shadow: shadow,
        },
        'image-figure',
      ]"
    >
      <slot> </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "ImageContainer",
  props: {
    round: {
      type: Boolean,
      default: false,
    },
    top: {
      type: Boolean,
      default: false,
    },
    bottom: {
      type: Boolean,
      default: false,
    },
    left: {
      type: Boolean,
      default: false,
    },
    right: {
      type: Boolean,
      default: false,
    },
    shadow: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style lang="scss">
.shadow {
  -webkit-box-shadow: 0px 10px 30px 0px rgba(34, 56, 80, 0.2);
  -moz-box-shadow: 0px 10px 30px 0px rgba(34, 60, 80, 0.2);
  box-shadow: 0px 10px 30px 0px rgba(34, 60, 80, 0.2);
}
.image-container {
  width: 100%;
  height: 100%;

  .image-figure {
    width: 100%;
    height: 100%;
    overflow: hidden;
    background: #fff;
  }
  .round-top {
    border-top-left-radius: 47%;
    border-top-right-radius: 47%;
  }
  .round-bottom {
    border-bottom-left-radius: 47%;
    border-bottom-right-radius: 47%;
  }
  .round-left {
    border-bottom-left-radius: 47%;
    border-top-left-radius: 47%;
  }
  .round-right {
    border-top-right-radius: 47%;
    border-bottom-right-radius: 47%;
  }
  .round {
    border-radius: 50%;
  }
}
</style>
