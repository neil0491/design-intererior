<template>
  <div class="container">
    <div class="slider-row">
      <div
        class="row slider-row__wrapper"
        v-for="(slide, index) in slides"
        :key="index"
      >
        <div class="col-5">
          <div class="left-slide" :class="activeSlide == index ? 'hidden' : ''">
            <TitleBlock
              :fs="3.25"
              :fw="900"
              :fwDesc="700"
              :title="slide.title"
              :description="slide.descr"
            >
              <Button class="mt-4" primary :text="slide.button" />
            </TitleBlock>
            <ImageContainer
              class="left-slide__image"
              style="height: 495px"
              bottom
            >
              <img :src="slide.imgLeft" alt="" srcset="" />
            </ImageContainer>
          </div>
        </div>

        <div class="col-7 right-corousel">
          <div
            class="right-slide"
            :class="activeSlide == index ? 'hidden' : ''"
          >
            <ImageContainer style="height: 775px" top>
              <img :src="slide.imgRight" alt="Slider" srcset="" />
            </ImageContainer>
          </div>
          <div>
            <div class="d-flex">
              <div class="right-corousel__control">Explore More</div>
              <div class="carousel__button">
                <button
                  @click="prevSlide"
                  :class="activeSlide !== 1 ? '' : 'btn-disable'"
                  class="btn-change btn-prev"
                ></button>
                <button
                  @click="nextSlide"
                  :class="
                    activeSlide !== this.slides.length ? '' : 'btn-disable'
                  "
                  class="btn-change btn-next"
                ></button>
              </div>
            </div>
            <div class="scroll-wrapper">
              <div
                class="scroll-wrapper__current"
                :style="{
                  width: 100 / slides.length + '%',
                  left: (100 / slides.length) * (activeSlide - 1) + '%',
                }"
              ></div>
            </div>
            <div class="carousel-current">
              <span>{{ activeSlide }}/{{ slides.length }}</span>
            </div>
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
  name: "Slider",
  components: { TitleBlock, ImageContainer, Button },
  data() {
    return {
      activeSlide: 1,
      slides: [
        {
          id: 1,
          imgLeft:
            "https://images.pexels.com/photos/4352247/pexels-photo-4352247.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          imgRight:
            "https://images.pexels.com/photos/2826787/pexels-photo-2826787.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          title: "Take our style ",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo repellat unde earum.",
          button: "All Process",
        },
        {
          id: 2,
          imgLeft:
            "https://images.pexels.com/photos/245208/pexels-photo-245208.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
          imgRight:
            "https://images.pexels.com/photos/3773579/pexels-photo-3773579.png?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          title: "Take our toure style",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo repellat unde earum.",
          button: " All Get Started",
        },
        {
          id: 3,
          imgLeft:
            "https://images.pexels.com/photos/1457847/pexels-photo-1457847.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          imgRight:
            "https://images.pexels.com/photos/3255245/pexels-photo-3255245.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          title: "Take our style quiz",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo repellat unde earum.",
          button: "Get Started",
        },
      ],
    }
  },
  methods: {
    nextSlide() {
      if (this.activeSlide < this.slides.length) this.activeSlide++
    },
    prevSlide() {
      if (this.activeSlide > 1) this.activeSlide--
    },
  },
}
</script>

<style scoped lang="scss">
@import "../../assets/scss/variables.scss";
@import "../../assets/scss/navigation-carousel-hero.scss";

.scroll-wrapper {
  width: 94%;
  height: 3px;
  margin: 1.5rem;
  background: #e0e6e8;
  position: relative;
  &__current {
    position: absolute;
    background: #0f393a;
    top: -1px;
    left: 0;
    width: 50%;
    height: 5px;
  }
}
.hidden {
  opacity: 0;
}
.carousel-current {
  padding: 0 1.5rem;
  font-size: 1.8rem;
  font-weight: 400;
}
.left-slide {
  margin-top: 8.4rem;
  width: 95%;
  height: 100%;
  background: $white;
  &__image {
    margin-top: 7rem;
  }
}
.right-slide {
  padding: 0 2rem;
}
.slider-row {
  position: relative;
  height: 1130px;
  &__wrapper {
    position: absolute;
    top: 0;
    left: 0;
  }
}
.right-corousel {
  &__control {
    padding: 0 2rem;
    margin-top: 3.5rem;
    font-size: 1.5rem;
    font-weight: bold;
    z-index: 10;
  }
  .carousel__button {
    display: flex;
    margin-top: 3rem;
    margin-left: auto;
    margin-right: 2rem;
  }
}
</style>
