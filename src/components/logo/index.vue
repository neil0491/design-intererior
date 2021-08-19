<template>
  <div class="logo">
    <span class="logo__up">Design</span> <br />
    <span class="logo__down">Interior</span>
    <div class="logo__img"></div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
.logo {
  color: #0f393a;
  &__up {
    font-weight: bold;
  }
  &__down {
    font-weight: bold;
    font-size: 1.5rem;
    line-height: 0.7;
  }
  &__img {
    margin-top: 5px;
    background: #0f393a;
    width: 88px;
    height: 65px;
    border-bottom-right-radius: 50px;
    border-bottom-left-radius: 50px;
  }
}
</style>
