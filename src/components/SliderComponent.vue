<template>
  <div>
    <div
      class="row justify-content-between slider-component align-items-center"
    >
      <div class="col-7">
        <TitleComponent
          class="slider-title m-0"
          :text="sliderObject.title"
          :priority="2"
        ></TitleComponent>
      </div>
      <div class="col-1">
        <div class="d-flex gap-1 align-items-center">
          <div class="slider-button"><i class="fas fa-arrow-left"></i></div>
          <div class="slider-button"><i class="fas fa-arrow-right"></i></div>
        </div>
      </div>
    </div>
    <div class="row justify-content-between slider-content align-items-center">
      <div class="col-12">
        <div class="d-flex overflow-hidden gap-4">
          <SliderCard
            v-for="(item, i) in sliderObject.itemList"
            :key="i + '-sliderItem'"
            :category="item.category"
            :imageSrc="item.image"
            :title="item.title"
            :imageAlt="item.alt"
          ></SliderCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SliderCard from "./SliderCard.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  name: "SliderComponent",
  components: { TitleComponent, SliderCard },
  props: {
    sliderObject: Object,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.slider-component {
  // padding: $padding-100 * 2 0;
  margin-bottom: 50px;
  .slider-title {
    color: white;
    margin-bottom: 50px;
  }
  .slider-button {
    background-color: $bg-grey;
    padding: 10px;
    color: white;
    // display: inline-block;
  }
}
</style>