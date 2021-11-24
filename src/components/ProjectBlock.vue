<template>
  <div class="container project-block">
    <ContextTitle :text="projectObject.contextTitle"></ContextTitle>
    <SliderComponent :sliderObject="projectObject.slider"></SliderComponent>
  </div>
</template>

<script>
import ContextTitle from "./ContextTitle.vue";
import SliderComponent from "./SliderComponent.vue";
export default {
  name: "ProjectBlock",
  components: { ContextTitle, SliderComponent },
  props: {
    projectObject: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.project-block {
  padding: $padding-100 * 2 0;
}
</style>