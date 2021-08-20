<template>
  <div class="dark-block">
    <div class="rectangele-up">
      <div class="rectangele-55"></div>
      <div class="rectangele-55"></div>
      <div class="rectangele-55"></div>
      <div class="rectangele-55"></div>
    </div>
    <div class="rectangele-down">
      <div class="rectangele-50"></div>
      <div class="rectangele-50"></div>
      <div class="rectangele-50"></div>
    </div>
    <div class="big-rectangele-down">
      <div class="rectangele-100"></div>
      <div class="rectangele-50"></div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-7">
          <TitleBlock
            class="mr-1"
            dark
            :fs="2.75"
            :fw="600"
            :fsDesc="1.2"
            :fwDesc="400"
            :mbTitle="1"
            title="Our affordable office interior design process"
            description="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet consectetur adipisicing elit."
          />

          <div class="d-flex flex-column image-wrapper">
            <ImageContainer style="height: 515px" top>
              <img
                src="https://images.pexels.com/photos/5806989/pexels-photo-5806989.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
                alt=""
                srcset=""
              />
            </ImageContainer>
            <TitleBlock
              class="mt-5"
              :mbTitle="1"
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
              class="mb-2"
              dark
              :mbTitle="1"
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
              />
            </ImageContainer>
            <TitleBlock
              class="mt-8 mb-3"
              :mbTitle="0"
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
@import "../../assets/scss/variables.scss";
// .rectangele-55 {
//   position: absolute;
//   top: 0;
//   right: 0;
// }
.dark-block {
  padding-top: 7.6rem;
  background-color: $primary-color;
  position: relative;
  z-index: -2;
  .rectangele-up {
    z-index: -1;
    position: absolute;
    top: 0;
    right: 90px;
    .rectangele-55:nth-child(2) {
      margin-left: 53px;
    }
    .rectangele-55:nth-child(3) {
      top: 140px;
      position: absolute;
      right: -90px;
      z-index: -1;
    }
  }
  .big-rectangele-down {
    position: absolute;
    bottom: 0;
    left: 0;
    z-index: -1;
    .rectangele-50 {
      position: absolute;
      bottom: 125px;
      left: 110px;
    }
  }
  .rectangele-down {
    position: absolute;
    bottom: 0;
    left: 250px;
    z-index: -1;
    .rectangele-50:nth-child(2) {
      margin-left: -44px;
    }
  }
  &__right {
    margin-top: 9.5rem;
    margin-bottom: 7rem;
    padding: 0 1rem;
  }
  &__button {
    margin-top: 4rem;
  }
}
.image-wrapper {
  margin-top: 17rem;
  margin-left: auto;
  margin-right: 3.3rem;
  max-width: 500px;
}

.rectangele-55 {
  width: 55px;
  height: 55px;
  background: white;
}
.rectangele-50 {
  width: 45px;
  height: 45px;
  background: white;
}
.rectangele-100 {
  width: 110px;
  height: 120px;
  background: white;
}
</style>
