<template>
  <div class="logo-wrapper">
    <div
      :class="{
        'logo-inner': true,
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
      frames: 4,
      currentFrame: 1,
      blinking: true
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
  height: 80px;
  overflow: hidden;
  width: 60px;
  .logo-inner {
    position: absolute;
    height: 80px;
    img {
      display: block;
      height: 80px;
      margin: 5px;
      max-height: initial;
    }
    &.blink {
      animation: logoblink 0.2s steps(8, end) alternate;
    }
  }
}
</style>
