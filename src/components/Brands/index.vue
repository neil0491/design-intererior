<template>
  <div class="brands">
    <div class="row">
      <div class="col d-flex flex-column justify-content-center">
        <div>
          <ImageContainer style="height: 180px" left>
            <img
              src="https://toppng.com/uploads/preview/jeep-grill-logo-png-image-jeep-brand-11562904368h9jov0hdtr.png"
            />
          </ImageContainer>
        </div>
      </div>
      <div class="col d-flex flex-column justify-content-center">
        <div class="p-2">
          <ImageContainer style="height: 180px" top>
            <img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
            />
          </ImageContainer>
        </div>
        <div class="p-2">
          <ImageContainer style="height: 180px" bottom
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
      </div>
      <div class="col d-flex flex-column justify-content-center">
        <div class="py-2 px-2">
          <ImageContainer style="height: 200px" top
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
        <div class="py-2 px-2">
          <ImageContainer style="height: 180px"
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
        <div class="py-2 px-2">
          <ImageContainer style="height: 200px" bottom
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
      </div>
      <div class="col d-flex flex-column justify-content-center">
        <div class="p-2">
          <ImageContainer style="height: 180px" top
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
        <div class="p-2">
          <ImageContainer style="height: 180px" bottom
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
      </div>
      <div class="col d-flex flex-column justify-content-center">
        <div>
          <ImageContainer style="height: 180px" right
            ><img
              src="https://image.neoseo.com.ua/image/catalog/foto_statti/topsovetovposozdanijubesplatnogologotipadljasajta/logo-design.png"
          /></ImageContainer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ImageContainer from "../Image-figure/index.vue"
export default {
  name: "Brands",
  components: { ImageContainer },
}
</script>

<style lang="scss" scoped>
.brands {
  max-width: 1200px;
  margin: 0 auto;
  margin-bottom: 6.6rem;
  // padding: 2rem;
  // min-height: 800px;
  &__title {
    text-align: center;
    font-family: "Franklin Gothic Medium", sans-serif;
    font-size: 2.5rem;
  }
}
</style>
