<template>
  <div class="testimonial-block">
    <div class="container">
      <ContextTitle
        :text="testimonialObject.contextTitle"
        :isCentered="true"
      ></ContextTitle>
      <div class="row justify-content-end">
        <div class="col-5">
          <TitleComponent
            class="testimonial-title"
            :priority="3"
            :text="testimonialObject.title"
          ></TitleComponent>
        </div>
      </div>
    </div>
    <div class="testimonials-row-container">
      <div class="container">
        <div class="bg-white">
          <div class="row justify-content-evenly">
            <div
              class="col-4"
              v-for="(testimonial, i) in testimonialObject.testimonialsList"
              :key="i + '-testimonial'"
            >
              <TestimonialCard
                :company="testimonial.company"
                :name="testimonial.name"
                :review="testimonial.review"
                :image="testimonial.img"
              ></TestimonialCard>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ContextTitle from "./ContextTitle.vue";
import TestimonialCard from "./TestimonialCard.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { ContextTitle, TitleComponent, TestimonialCard },
  name: "TestimonialBlock",
  props: { testimonialObject: Object },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.testimonial-block {
  padding-bottom: 200px;
  .testimonial-context-title {
    text-align: end;
  }
  .testimonials-row-container {
    background: linear-gradient(
      90deg,
      $bg-dark 0%,
      $bg-dark 50%,
      white 53%,
      white 100%
    );
  }
  .testimonial-title {
    color: white;
    text-align: end;
    font-weight: bold;
    margin-bottom: 50px;
  }
}
</style>