<template>
  <div class="d-flex align-items-baseline gap-2">
    <div class="line-element"></div>
    <h6>{{ text }}</h6>
  </div>
</template>

<script>
export default {
  name: "ContextTitle",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.line-element {
  border-bottom: 3px solid greenyellow;
  width: 40px;
}
h6 {
  vertical-align: bottom;
  text-transform: uppercase;
  color: white;
}
</style>