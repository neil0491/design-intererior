<template>
  <canvas class="footer-circule"> </canvas>
</template>

<script>
export default {
  name: "Circule-Footer",
  data: () => ({
    vueCanvas: null,
    painting: false,
    canvas: null,
    ctx: null,
    size: 500,
    stroke: 110,
  }),
  mounted() {
    this.canvas = document.querySelector(".footer-circule")
    this.ctx = this.canvas.getContext("2d")

    // Resize canvas
    this.canvas.height = 210
    this.canvas.width = 385
    this.ctx.beginPath()

    this.ctx.lineWidth = this.stroke
    this.ctx.arc(100, 280, 210, 0, 2 * Math.PI)
    this.ctx.strokeStyle = "#e7ebec"
    this.ctx.stroke()
    this.ctx.lineWidth = 1
    this.ctx.fillStyle = "#fff"
    this.ctx.fillRect(85, 5, 40, 35)
    this.ctx.fillRect(145, 25, 18, 18)
    this.ctx.fillRect(125, 40, 18, 18)
    this.ctx.fillRect(215, 179, 40, 45)
    this.ctx.fillRect(255, 160, 18, 18)
    this.ctx.fillRect(240, 145, 18, 18)
  },
}
</script>
