<template>
  <div class="logo-wrapper">
    <div
      :class="{
        'logo-inner': false,
        blink: blinking
      }"
    >
      <img
        v-for="x in frames"
        :key="x"
        :src="`/logo-frames/logo-f${x - 1}.svg`"
      />
      <img
        v-for="x in frames"
        :key="`${x}-r`"
        :src="`/logo-frames/logo-f${frames - x}.svg`"
      />
    </div>
  </div>
</template>
<script>
export default {
  name: 'SiteLogo',
  data() {
    return {
      frames: 9,
      currentFrame: 1,
      blinking: false
    }
  },
  mounted() {
    setInterval(() => {
      const rand = Math.ceil(Math.random() * 10)
      this.blinking = rand % 2
    }, 1000)
  }
}
</script>
<style lang="scss">
@keyframes logoblink {
  100% {
    transform: translateY(-360px);
  }
}
.logo-wrapper {
  position: relative;
  height: 200px;
  overflow: hidden;
  width: 200px;
  .logo-inner {
    position: absolute;
    height: 2000px;
    img {
      display: block;
      height: 200px;
      margin: 5px;
      max-height: initial;
    }
    &.blink {
      animation: logoblink 0.2s steps(8, end) alternate;
    }
  }
}
</style>
