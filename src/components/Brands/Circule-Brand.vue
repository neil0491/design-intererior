<template>
  <canvas class="circule-canvas"> </canvas>
</template>

<script>
export default {
  name: "Circule-Brand",
  data: () => ({
    vueCanvas: null,
    painting: false,
    canvas: null,
    ctx: null,
    size: 500,
    stroke: 100,
  }),
  mounted() {
    this.canvas = document.querySelector(".circule-canvas")
    this.ctx = this.canvas.getContext("2d")

    // Resize canvas
    this.canvas.height = 500
    this.canvas.width = 350
    this.ctx.beginPath()

    this.ctx.lineWidth = this.stroke
    this.ctx.arc(275, 250, 200, 0, 2 * Math.PI)
    this.ctx.strokeStyle = "#0f393a"
    this.ctx.stroke()
    this.ctx.lineWidth = 1
    this.ctx.fillStyle = "#fff"
    this.ctx.fillRect(240, 0, 40, 35)
    this.ctx.fillRect(208, 16, 18, 18)
    this.ctx.fillRect(225, 30, 18, 18)
    this.ctx.fillRect(105, 190, 30, 35)
    this.ctx.fillRect(105, 160, 18, 18)
    this.ctx.fillRect(90, 175, 18, 18)
  },
}
</script>
