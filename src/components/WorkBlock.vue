<template>
  <div class="work-block">
    <TitleComponent
      class="work-title"
      :priority="3"
      :text="workObject.title"
      style="text-align: center"
    >
    </TitleComponent>
    <p class="work-description">{{ workObject.description }}</p>
    <ButtonComponent
      class="work-button"
      :text="workObject.button.text"
      :href="workObject.button.href"
    ></ButtonComponent>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { TitleComponent, ButtonComponent },
  name: "WorkBlock",
  props: {
    workObject: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.work-block {
  background-image: url("../assets/business-people-working-together-on-project-and-B3MZ4TX.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  padding: 100px 0;
  .work-title {
    color: white;
  }
  .work-description {
    text-align: center;
    margin: auto;
    width: 400px;
    color: white;
    font-size: 14px;
    margin-bottom: 20px;
  }
  .work-button {
    color: white;
    background-color: $bg-dark;
  }
}
</style>