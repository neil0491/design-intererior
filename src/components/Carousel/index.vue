<template>
  <div class="carousel">
    <div class="container">
      <h3 class="title-caousel">
        Read our tips on designing and furnishing your office
      </h3>
    </div>
    <div class="slider">
      <swiper
        navigation
        :slides-per-view="3"
        :space-between="30"
        :centeredSlides="true"
      >
        <swiper-slide v-for="slide in slides" :key="slide.id">
          <div class="slider__carousel">
            <img class="slider__image mb-4" :src="slide.url" alt="Interior" />
            <h4 class="slider__title">{{ slide.title }}</h4>
            <p class="slider__descr">{{ slide.descr }}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue"
import SwiperCore, { Navigation } from "swiper"
SwiperCore.use([Navigation])

// Import Swiper styles
// import "swiper/swiper.scss"

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data: () => ({
    slides: [
      {
        id: 1,
        title: "Choosing your office furniture in 2021",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 2,
        title: "How to Choosing Furniture For Your Office",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus doloreur adipisicing elit",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 3,
        title: "Choosing The Right Office Chair",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 4,
        title: "How to Choosing Furniture For Your Office",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 5,
        title: "Choosing your office furniture in 2021",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 6,
        title: "Choosing The Right Office Chair",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
      {
        id: 7,
        title: "How to Choosing Furniture For Your Office",
        descr:
          "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto eum maxime voluptatem debitis accusamus dolore.",
        url: "https://images.pexels.com/photos/7046164/pexels-photo-7046164.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";
@import "../../assets/scss/navigation-carousel.scss";

.carousel {
  background-color: rgba($color: #f7fdfd, $alpha: 0.9);
  padding: 5rem 0 4rem;
}
.title-caousel {
  max-width: 800px;
  font-size: 2.7rem;
  line-height: 1.5;
  font-weight: bold;
  margin-bottom: 5rem;
}
.slider {
  margin-left: 2rem;
  &__carousel {
  }
  &__image {
    height: 250px;
  }
  &__title {
    font-size: 2rem;
    font-weight: 700;
    line-height: 1.5;
  }
  &__descr {
    line-height: 1.4;
    font-size: 1.2rem;
    color: $secondary-text;
  }
}
// .swiper-button-prev {
//   left: auto;
//   right: 0;
//   top: 0;
//   background: rebeccapurple;
//   background-image: url("/img/arrow-left.svg");
//   background-repeat: no-repeat;
//   background-position: center;
// }
// .swiper-button-prev::after,
// .swiper-button-next::after {
//   // content: "";
// }
// .swiper-button-next {
//   // right: 30px;
//   // top: 845px;

//   background-image: url("/img/arrow-right.svg");
//   background-repeat: no-repeat;
//   background-position: center;
// }
// .swiper-button-prev,
// .swiper-button-next {
//   border: 1px solid $primary-color;
//   border-radius: 50%;
//   // background: cornflowerblue;
//   width: 45px;
//   height: 45px;
// }

// .swiper-pagination {
//   bottom: 180px;
//   left: 0;
//   width: 15%;
//   font-size: 1.5rem;
//   font-weight: bold;
// }
</style>
