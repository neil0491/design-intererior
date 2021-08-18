<template>
  <div>
    <Header />
    <Slider />
    <Quote />
    <Brands />
    <ChooseUs />
    <DesignProcess />
    <Packages />
  </div>
</template>

<script>
import Header from "./components/Header"
import Slider from "./components/Slider"
import Quote from "./components/Quote"
import Brands from "./components/Brands"
import ChooseUs from "./components/ChooseUs"
import DesignProcess from "./components/DesignProcess"
import Packages from "./components/Packages"

export default {
  name: "App",
  components: {
    Header,
    Slider,
    Quote,
    Brands,
    ChooseUs,
    DesignProcess,
    Packages,
  },
}
</script>

<style lang="scss"></style>
