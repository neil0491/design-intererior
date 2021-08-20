<template>
  <div class="quote">
    <div class="quote__text">
      "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo
      repellat sequi molestiae eius unde earum.
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";

.quote {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 8rem;
  padding-bottom: 6rem;
  text-align: center;
  // min-height: 450px;
  font-size: 2.5em;
  font-weight: 700;
  line-height: 1.5;
  &__text {
    max-width: 960px;
  }
}
</style>
