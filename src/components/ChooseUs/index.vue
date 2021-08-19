<template>
  <div class="choose-block">
    <div class="container">
      <div class="row">
        <div class="col-6">
          <TitleBlock
            class="mb-5"
            :fs="2.65"
            :fw="700"
            :fsDesc="1.2"
            :fwDesc="400"
            title="Why Choose Us?"
            description="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet consectetur adipisicing elit. Officiis nam quas possimus quae."
          />
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-3">
          <IterebleBlock
            :number="1"
            title="No hassle"
            descr="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet"
          />
        </div>
        <div class="col-3">
          <IterebleBlock
            :number="2"
            title="Saving"
            descr="Lorem, ipsum dolor adipisicing ipsum consectetur adipisicing elit. Officia vitae,onsectetur adipisicing amet"
          />
        </div>
        <div class="col-3">
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
import TitleBlock from "../Title-Block/index.vue"
import IterebleBlock from "../Itereble-block/index.vue"
export default {
  name: "ChooseUs",
  components: { TitleBlock, IterebleBlock },
}
</script>

<style lang="scss" scoped>
.choose-block {
  background-color: rgba($color: #f7fdfd, $alpha: 0.9);
  padding-top: 4.5rem;
  padding-bottom: 5rem;
}
</style>
