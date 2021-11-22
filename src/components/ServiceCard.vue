<template>
  <div class="d-flex">
    <div>
      <i class="fas" :class="iconClass"></i>
    </div>
    <section class="service-card-text-section">
      <TitleComponent :priority="5" :text="title"></TitleComponent>
      <p>{{ description }}</p>
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
i {
  font-size: 35px;
  color: white;
  background-color: red;
  padding: 10px;
  border-radius: 50%;
}
.service-card-text-section {
  padding: 0 35px;
}
</style>