<template>
  <div class="container">
    <div class="row package">
      <div class="col pr-8">
        <ImageContainer style="height: 674px" top>
          <img
            src="https://images.pexels.com/photos/5806989/pexels-photo-5806989.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
            alt=""
            srcset=""
          />
        </ImageContainer>
      </div>
      <div class="col d-flex">
        <TitleBlock
          class="mt-auto"
          :fs="2.8"
          :fw="700"
          :fsDesc="1.2"
          :fwDesc="400"
          title="Office Interior Design Packages"
          description="Lorem ipsum dolor sit. Totam earum vitae accusantium reiciendis provident consequatur hic eaque mollitia nobis molestias, impedit, aliquam rerum, saepe doloribus cumque maiores sit obcaecati ducimus?"
        >
          <Button class="mt-4" primary text="See Package" />
        </TitleBlock>
      </div>
    </div>
  </div>
</template>

<script>
import TitleBlock from "../Title-Block/index.vue"
import ImageContainer from "../Image-figure/index.vue"
import Button from "../Button/Button.vue"
export default {
  name: "Packages",
  components: { TitleBlock, ImageContainer, Button },
}
</script>

<style lang="scss" scoped>
.package {
  padding: 8rem 0;
}
</style>
