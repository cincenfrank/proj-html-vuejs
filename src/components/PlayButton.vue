<template>
  <div class="play-container"><div class="play"></div></div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.play-container {
  border: 2px solid white;
  padding: 10px;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
  .play {
    border-top: 7px solid transparent;
    border-bottom: 7px solid transparent;
    border-left: 14px solid $accent-color;
    height: 0px;
  }
}
</style>