<template>
  <div class="dark-block">
    <div class="container">
      <div class="row">
        <div class="col-7">
          <div>
            <TitleBlock
              dark
              :fs="2.75"
              :fw="600"
              :fsDesc="1.2"
              :fwDesc="400"
              title="Our affordable office interior design process"
              description="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet consectetur adipisicing elit."
            />
          </div>
          <div class="d-flex flex-column image-wrapper">
            <ImageContainer style="height: 515px" top>
              <img
                src="https://images.pexels.com/photos/5806989/pexels-photo-5806989.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
                alt=""
                srcset=""
              />
            </ImageContainer>
            <TitleBlock
              class="mt-4"
              dark
              :fs="1.5"
              :fw="500"
              :fsDesc="1"
              :fwDesc="400"
              title="We send you an estimate within 24 hour"
              description="Lorem ipsum dolor sit. Totam earum vitae accusantium reiciendis provident consequatur hic eaque mollitia nobis molestias, impedit, aliquam rerum, saepe doloribus cumque maiores sit obcaecati ducimus?"
            >
              <Button class="dark-block__button" text="View All Process" />
            </TitleBlock>
          </div>
        </div>
        <div class="col-5">
          <div class="dark-block__right">
            <TitleBlock
              dark
              :fs="1.5"
              :fw="700"
              :fsDesc="1"
              :fwDesc="400"
              title="Take our style quiz"
              description="Lorem ipsum dolor sit.
            Totam earum vitae accusantium reiciendis provident consequatur hic
            eaque."
            />
            <ImageContainer style="height: 500px" round>
              <img
                src="https://images.pexels.com/photos/5806989/pexels-photo-5806989.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
                alt=""
                srcset=""
              />
            </ImageContainer>
            <TitleBlock
              class="mt-5"
              dark
              :fs="1.5"
              :fw="700"
              :fsDesc="1"
              :fwDesc="400"
              title="Your projext kicks off!"
              description="Lorem ipsum dolor sit.Totam earum vitae accusantium reiciendis provident.
            Totam earum vitae accusantium reiciendis provident consequatur hic
            eaque."
            />
            <ImageContainer style="height: 500px" bottom>
              <img
                src="https://images.pexels.com/photos/5806989/pexels-photo-5806989.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
                alt=""
                srcset=""
              />
            </ImageContainer>
          </div>
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
  components: { TitleBlock, ImageContainer, Button },
}
</script>

<style lang="scss" scoped>
.dark-block {
  padding-top: 7.6rem;
  background-color: $primary-color;
  &__right {
    margin-top: 9.5rem;
    margin-bottom: 7rem;
  }
  &__button {
    margin-top: 4rem;
  }
}
.image-wrapper {
  margin-top: 16rem;
  margin-left: auto;
  margin-right: 2.5rem;
  max-width: 500px;
}
</style>
