<template>
  <div class="block" :class="{ dark: dark }">
    <h2
      class="block__title mb-4"
      :style="{ fontSize: fs + 'rem', fontWeight: fw }"
    >
      {{ title }}
    </h2>
    <p
      class="block__description light-color"
      :style="{ fontSize: fsDesc + 'rem', fontWeight: fwDesc }"
    >
      {{ description }}
    </p>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Title-Block",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    fs: {
      type: Number,
      required: false,
    },
    fw: {
      type: Number,
      required: false,
    },
    fsDesc: {
      type: Number,
      required: false,
    },
    fwDesc: {
      type: Number,
      required: false,
    },
    dark: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";

.dark {
  .block__title {
    color: $white;
  }
  .block__description {
    color: $dark-text;
  }
}
.block {
  &__title {
    // font-size: 3.25rem;
    // font-weight: 900;
    line-height: 1.7;
  }
  &__description {
    line-height: 2rem;
    font-size: 1.2rem;
    color: $secondary-text;
  }
}
</style>
