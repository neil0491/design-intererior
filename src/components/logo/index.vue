<template>
  <div class="logo">
    <span class="logo__up">Design</span> <br />
    <span class="logo__down">Interior</span>
    <div class="logo__img">
      <div class="rectangele-1"></div>
      <div class="rectangele-2"></div>
      <div class="rectangele-3"></div>
    </div>
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
    position: relative;
    .rectangele-1 {
      width: 11px;
      height: 11px;
      position: absolute;
      top: 0;
      right: 20px;
      background: #fff;
    }
    .rectangele-2 {
      width: 15px;
      height: 15px;
      position: absolute;
      top: 10px;
      right: 30px;
      background: #fff;
    }
    .rectangele-3 {
      width: 6px;
      height: 6px;
      position: absolute;
      top: 25px;
      right: 25px;
      background: #fff;
    }
  }
}
</style>
