<template>
  <div class="container">
    <div class="row">
      <div class="col-5">
        <div class="left-slide">
          <TitleBlock
            :fs="3.25"
            :fw="900"
            :fwDesc="700"
            title="Office Design Made Affordable."
            description="Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia vitae, officiis nam quas possimus quae."
          >
            <Button class="mt-4" primary text="Get Started" />
          </TitleBlock>
          <ImageContainer
            class="left-slide__image"
            style="height: 495px"
            bottom
          ></ImageContainer>
        </div>
      </div>

      <div class="col-7">
        <div class="right-slide">
          <ImageContainer style="height: 775px" top></ImageContainer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TitleBlock from "../Title-Block/index.vue"
import ImageContainer from "../Image-figure/index.vue"
import Button from "../Button/Button.vue"
export default {
  name: "Slider",
  components: { TitleBlock, ImageContainer, Button },
}
</script>

<style lang="scss">
.left-slide {
  margin-top: 8.4rem;
  width: 95%;
  &__image {
    margin-top: 7rem;
  }
}
.right-slide {
  padding: 0 2rem;
}
</style>
