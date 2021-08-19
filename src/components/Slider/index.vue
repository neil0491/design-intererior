<template>
  <div class="container">
    <div class="row">
      <div class="col-5">
        <swiper
          :slides-per-view="1"
          @swiper="setFirstSwiper"
          :controller="{ control: secondSwiper }"
          effect="fade"
        >
          <swiper-slide v-for="slide in slideleft" :key="slide.id">
            <div class="left-slide">
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
                <img :src="slide.img" alt="" srcset="" />
              </ImageContainer>
            </div>
          </swiper-slide>
        </swiper>
      </div>

      <div class="col-7 right-corousel">
        <swiper
          :slides-per-view="1"
          @swiper="setSecondSwiper"
          :controller="{ control: firstSwiper }"
          navigation
          :pagination="{ type: 'fraction' }"
          :scrollbar="{ draggable: true }"
          effect="fade"
          noSwipingClass="swiper-no-swiping"
        >
          <swiper-slide v-for="(slide, index) in slideRight" :key="index">
            <div class="right-slide">
              <ImageContainer style="height: 775px" top>
                <img :src="slide" alt="Slider" srcset="" />
              </ImageContainer>
            </div>
          </swiper-slide>
        </swiper>
        <div class="right-corousel__control">Explore More</div>
      </div>
    </div>
  </div>
</template>

<script>
import TitleBlock from "../Title-Block/index.vue"
import ImageContainer from "../Image-figure/index.vue"
import Button from "../Button/Button.vue"

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue"
import SwiperCore, {
  Controller,
  EffectFade,
  Navigation,
  Pagination,
  Scrollbar,
} from "swiper"
SwiperCore.use([Controller, EffectFade, Navigation, Pagination, Scrollbar])

import "swiper/swiper.scss"
// import "swiper/components/navigation/navigation.scss"

import "swiper/components/pagination/pagination.scss"
import "swiper/components/scrollbar/scrollbar.scss"

export default {
  name: "Slider",
  components: { TitleBlock, ImageContainer, Button, Swiper, SwiperSlide },
  data() {
    return {
      firstSwiper: null,
      secondSwiper: null,
      slideleft: [
        {
          id: 1,
          img: "https://images.pexels.com/photos/3356416/pexels-photo-3356416.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          title: "Take our style quiz",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo repellat sequi molestiae eius unde earum.",
          button: "Get Started",
        },
        {
          id: 2,
          img: "https://images.pexels.com/photos/2227832/pexels-photo-2227832.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          title: "Office Design Made Affordable.",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.Perferendis nemo repellat sequi molestiae eius adipisicing elit.",
          button: "View All Process",
        },
        {
          id: 3,
          img: "https://images.pexels.com/photos/3773579/pexels-photo-3773579.png?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
          title: "Office Design Made Affordable.",
          descr:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis nemo repellat sequi molestiae eius unde earum.",
          button: "Get Started",
        },
      ],
      slideRight: [
        "https://images.pexels.com/photos/3773579/pexels-photo-3773579.png?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
        "https://images.pexels.com/photos/3255245/pexels-photo-3255245.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
        "https://images.pexels.com/photos/3952038/pexels-photo-3952038.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260",
      ],
    }
  },
  methods: {
    setFirstSwiper(swiper) {
      this.firstSwiper = swiper
    },
    setSecondSwiper(swiper) {
      this.secondSwiper = swiper
    },
  },
}
</script>

<style lang="scss">
@import "../../assets/scss/variables.scss";
@import "../../assets/scss/navigation-carousel-hero.scss";

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
.swiper-container {
  height: 100%;
}
.swiper-button-prev {
  left: auto;
  right: 90px;
  top: 845px;
  background-image: url("/img/arrow-left.svg");
  background-repeat: no-repeat;
  background-position: center;
}
.swiper-button-prev::after,
.swiper-button-next::after {
  content: "";
}
.swiper-button-next {
  right: 30px;
  top: 845px;

  background-image: url("/img/arrow-right.svg");
  background-repeat: no-repeat;
  background-position: center;
}
.swiper-button-prev,
.swiper-button-next {
  border: 1px solid $primary-color;
  border-radius: 50%;
  // background: cornflowerblue;
  width: 45px;
  height: 45px;
}
.right-corousel {
  position: relative;
  &__control {
    position: absolute;
    top: 830px;
    left: 40px;
    font-size: 1.5rem;
    font-weight: bold;
  }
}
.swiper-scrollbar {
  bottom: 231px !important;
  left: 1.8rem !important;
  width: 93% !important;
}
.swiper-pagination {
  bottom: 180px;
  left: 0;
  width: 15%;
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
