<template>
  <div class="carousel">
    <div class="container">
      <div class="d-flex">
        <h3 class="title-caousel">
          Read our tips on designing and furnishing your office
        </h3>
        <div class="carousel__button">
          <button
            class="btn-change btn-prev"
            :class="activeSlide !== 1 ? '' : 'btn-disable'"
            @click="prevSlide"
          ></button>
          <button
            class="btn-change btn-next"
            :class="activeSlide !== this.slides.length ? '' : 'btn-disable'"
            @click="nextSlide"
          ></button>
        </div>
      </div>
    </div>
    <div class="slider">
      <div class="slider__wrap" :style="{ width: 500 * slides.lenght }">
        <div
          class="slider__slide"
          :style="styleObject"
          v-for="(slide, index) in slides"
          :key="index"
        >
          <img class="slider__image mb-4" :src="slide.url" alt="Interior" />
          <h4 class="slider__title">{{ slide.title }}</h4>
          <p class="slider__descr">{{ slide.descr }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    activeSlide: 1,
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
  computed: {
    styleObject() {
      const width = 0 - (this.activeSlide - 1) * 350
      return {
        transform: "translateX(" + width + "px)",
      }
    },
  },
  methods: {
    nextSlide: function () {
      if (this.activeSlide < this.slides.length) this.activeSlide++
    },
    prevSlide: function () {
      if (this.activeSlide > 1) this.activeSlide--
    },
  },
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/variables.scss";
@import "../../assets/scss/navigation-carousel.scss";

.carousel {
  background-color: rgba($color: #f7fdfd, $alpha: 0.9);
  padding: 5rem 0 4rem;
  &__button {
    border: none;
  }
  &__button {
    margin-top: auto;
    margin-bottom: auto;
    margin-left: auto;
  }
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
  overflow: hidden;
  &__wrap {
    width: 2800px;
    display: flex;
    flex-wrap: nowrap;
    flex-direction: row;
  }
  &__slide {
    margin: 0 1rem;
    width: 500px;
    transition: all 0.5s ease-in-out;
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
</style>
