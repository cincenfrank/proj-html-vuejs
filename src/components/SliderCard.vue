<template>
  <div class="slider-card position-relative">
    <img :src="imageSrc" :alt="imageAlt" />
    <div class="slider-card-overlay position-absolute bottom-0 start-0 end-0">
      <div class="d-flex justify-content-between align-items-center">
        <div>
          <h6 class="slider-card-title">{{ title }}</h6>
          <p class="slider-card-category">{{ category }}</p>
        </div>
        <div class="slider-card-button"><i class="fas fa-plus"></i></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderCard",
  props: {
    imageSrc: String,
    imageAlt: String,
    title: String,
    category: String,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.slider-card {
  width: 33%;
  flex-shrink: 0;
  text-align: left;

  img {
    object-fit: contain;
    width: 100%;
    transition: all 0.3s 0.3s;
  }
  .slider-card-overlay {
    opacity: 0;
    color: white;
    padding: 0 30px;
    transition: all 0.3s;
    .slider-card-title {
      font-weight: bold;
      text-transform: capitalize;
    }
    .slider-card-category {
      color: $light-text-color;
    }
    .slider-card-button {
      padding: 10px;
      background-color: $bg-dark;
      cursor: pointer;
    }
  }
  &:hover {
    img {
      filter: grayscale(100%) brightness(40%) sepia(100%) hue-rotate(-50deg)
        saturate(600%) contrast(0.8);
      transition: all 0.3s;
    }
    .slider-card-overlay {
      opacity: 1;
      transition: all 0.3s 0.3s;
    }
  }
}
</style>