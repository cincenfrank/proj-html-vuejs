<template>
  <div class="d-flex">
    <div>
      <i class="fas" :class="iconClass"></i>
    </div>
    <section class="service-card-text-section">
      <TitleComponent :priority="5" :text="title"></TitleComponent>
      <p class="service-card-description">{{ description }}</p>
    </section>
  </div>
</template>

<script>
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { TitleComponent },
  name: "ServiceCard",
  props: { title: String, description: String, iconClass: String },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
i {
  font-size: 20px;
  color: white;
  background-color: $primary-color;
  padding: 15px;
  border-radius: 50%;
}
.service-card-text-section {
  padding: 0 30px;
  text-align: left;
  .service-card-description {
    font-size: 12px;
    padding: 10px 0 0;
    color: $secondary-color;
  }
}
</style>