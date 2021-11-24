<template>
  <div
    class="d-flex align-items-baseline gap-2 context-title"
    :class="isCentered ? 'justify-content-center position-relative' : ''"
  >
    <div
      class="line-element"
      :class="isCentered ? 'position-absolute end-0' : ''"
    ></div>
    <h6>{{ text }}</h6>
  </div>
</template>

<script>
export default {
  name: "ContextTitle",
  props: {
    text: String,
    isCentered: { default: false },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.context-title {
  margin-bottom: 15px;
  .line-element {
    border-bottom: 3px solid $accent-color;
    width: 40px;
  }
  h6 {
    font-size: 14px;
    vertical-align: bottom;
    text-transform: uppercase;
    color: white;
  }
}
</style>