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
          <div class="slider-button" @click="onPreviousItem">
            <i class="fas fa-arrow-left"></i>
          </div>
          <div class="slider-button" @click="onNextItem">
            <i class="fas fa-arrow-right"></i>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-content-between slider-content align-items-center">
      <div class="col-12">
        <div class="d-flex overflow-hidden gap-4">
          <!-- <SliderCard
            v-for="(item, i) in sliderObject.itemList"
            :key="i + '-sliderItem'"
            :category="item.category"
            :imageSrc="item.image"
            :title="item.title"
            :imageAlt="item.alt"
          ></SliderCard> -->
          <SliderCard
            v-for="(index, i) in itemIndexList"
            :key="i + '-sliderItem'"
            :category="sliderObject.itemList[index].category"
            :imageSrc="sliderObject.itemList[index].image"
            :title="sliderObject.itemList[index].title"
            :imageAlt="sliderObject.itemList[index].alt"
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
    return {
      itemToShow: 3,
      currentMaxItemIndex: 2,
    };
  },
  computed: {
    startingMaxItemIndex() {
      return this.itemToShow - 1;
    },
    itemIndexList() {
      const toReturn = [];
      for (let index = 1; index <= this.itemToShow; index++) {
        toReturn.push(this.currentMaxItemIndex - this.itemToShow + index);
      }
      return toReturn;
    },
  },
  methods: {
    onNextItem() {
      if (this.currentMaxItemIndex < this.sliderObject.itemList.length - 1) {
        this.currentMaxItemIndex++;
      }
    },
    onPreviousItem() {
      if (this.currentMaxItemIndex > this.startingMaxItemIndex) {
        this.currentMaxItemIndex--;
      }
    },
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
    cursor: pointer;
    // display: inline-block;
  }
}
</style>