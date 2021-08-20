<template>
  <header class="container header">
    <div class="row">
      <div class="col-6">
        <a class="header__logo" href="/"> <Logo /> </a>
      </div>
      <div class="col-6">
        <ul class="list">
          <li class="list__item">
            <a class="list__link active" href="#">Home</a>
          </li>
          <li class="list__item">
            <a class="list__link" href="#">About Us</a>
          </li>
          <li class="list__item"><a class="list__link" href="#">Service</a></li>
          <li class="list__item"><a class="list__link" href="#">Contact</a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
import Logo from "../logo"
export default {
  name: "Header",
  components: {
    Logo,
  },
}
</script>

<style lang="scss" scoped>
.header {
  height: 110px;
  font-weight: 600;
  margin-top: 2rem;
  &__logo {
    display: block;
    width: 90px;
    height: 95px;
  }
}
.list {
  display: flex;
  align-items: center;
  list-style: none;
  height: 100%;
  font-size: 1.1rem;
  margin: 0 3rem;
  &__item {
    margin-right: 3.2rem;
  }
  &__link {
    position: relative;
    color: inherit;
    text-decoration: none;
    cursor: pointer;
  }
  &__link.active::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    width: 36px;
    height: 36px;
    background: #e0e6e8;
    border-radius: 50%;
    transform: translate(-50%, -50%);
    z-index: -1;
  }
}
</style>
