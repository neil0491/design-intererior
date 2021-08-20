<template>
  <div class="choose-block">
    <div class="container">
      <div class="row">
        <div class="col-6">
          <div class="choose">
            <h3 class="choose__title">Why Choose Us?</h3>
            <p class="choose__descr">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
              voluptates aut expedita quasi odit ipsum rem temporibus aut
              expedita quasi odit impedit odio perferendis.
            </p>
          </div>
        </div>
      </div>
      <div class="iter">
        <div class="iter__item">
          <IterebleBlock
            :number="1"
            title="No hassle"
            descr="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet"
          />
        </div>
        <div class="iter__item">
          <IterebleBlock
            :number="2"
            title="Saving"
            descr="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet"
          />
        </div>
        <div class="iter__item">
          <IterebleBlock
            :number="3"
            title="Choice"
            descr="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import TitleBlock from "../Title-Block/index.vue"
import IterebleBlock from "../Itereble-block/index.vue"
export default {
  name: "ChooseUs",
  components: { IterebleBlock },
}
</script>

<style lang="scss" scoped>
.choose {
  &__title {
    font-size: 2.65rem;
    font-weight: 700;
  }
  &__descr {
    margin-top: 2rem;
    font-size: 1.2rem;
    line-height: 1.6;
  }
}
.iter {
  display: flex;
  margin: 2.3rem -0.3rem 0;
  &__item {
    flex: 0 0 320px;
    margin-right: 2.7rem;
  }
}
.choose-block {
  background-color: rgba($color: #f7fdfd, $alpha: 0.9);
  padding-top: 6.3rem;
  padding-bottom: 6rem;
}
</style>
