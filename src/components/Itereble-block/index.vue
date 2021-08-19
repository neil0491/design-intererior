<template>
  <div class="iter d-flex flex-column">
    <span class="iter__number">0{{ number }}</span>
    <h4 class="iter__title">{{ title }}</h4>
    <p class="iter__description">{{ descr }}</p>
  </div>
</template>

<script>
export default {
  name: "Itereble-block",
  props: {
    number: {
      type: Number,
      requaired: true,
    },
    title: {
      type: String,
      requaired: true,
    },
    descr: {
      type: String,
      requaired: true,
    },
  },
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";

.iter {
  &__number {
    font-weight: 900;
    font-size: 2.75rem;
    color: $secondary-text;
    line-height: 1.5;
  }
  &__title {
    font-weight: 700;
    font-size: 1.75rem;
  }
  &__description {
    line-height: 1.5;
    color: $secondary-color;
  }
}
</style>
