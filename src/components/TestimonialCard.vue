<template>
  <div class="testimonial-card">
    <img :src="image" :alt="name + ' picture'" />
    <div class="text-block">
      <p class="review">{{ review }}</p>
      <h6 class="name">{{ name }}</h6>
      <em class="company">{{ company }}</em>
    </div>
  </div>
</template>

<script>
export default {
  name: "TestimonialCard",
  props: {
    review: String,
    company: String,
    name: String,
    image: String,
  },
};
</script>

<style lang="scss" scoped>
.testimonial-card {
  position: relative;
  cursor: pointer;
  // padding: 0 50px;

  // height: 100%;
  img {
    opacity: 0;
    width: 100%;
    transition: all 0.5s;
  }

  .text-block {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 0 50px;
    transition: all 0.3s;
    text-align: left;
    // object-fit: cover;

    // z-index: 0;
    // z-index: 0;
    .review {
      font-size: 14px;
      padding: 50px 0;
    }
    .name {
      color: black;
      font-weight: bold;
      text-transform: capitalize;
      font-size: 18px;
      margin: 0;
    }
    .company {
      text-transform: capitalize;
    }
  }
  &:hover {
    img {
      opacity: 1;
    }
    .text-block {
      color: white;
      .name {
        color: white;
      }
    }
  }
}
</style>