<template>
  <div>
    <section class="about-us-section">
      <div class="container">
        <div class="row justify-content-end">
          <div class="col-5">
            <div class="about-us-text-section">
              <ContextTitle :text="aboutUsObject.contextTitle"></ContextTitle>
              <TitleComponent
                class="about-us-title"
                :priority="2"
                :text="aboutUsObject.title"
              ></TitleComponent>
              <p class="about-us-text-description">
                {{ aboutUsObject.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="call-to-action">
      <div class="call-to-action-content container p-0">
        <div class="row justify-content-evenly">
          <div class="col-4">
            <TitleComponent
              class="call-to-action-title"
              :priority="3"
              :text="aboutUsObject.callToAction.text"
            ></TitleComponent>
          </div>
          <div class="col-4">
            <p class="call-to-action-description">
              {{ aboutUsObject.callToAction.description }}
            </p>
          </div>
        </div>

        <ButtonComponent
          class="flex-grow-0 call-to-action-button"
          :text="aboutUsObject.callToAction.button.text"
          :href="aboutUsObject.callToAction.button.href"
        ></ButtonComponent>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
import ContextTitle from "./ContextTitle.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { ContextTitle, TitleComponent, ButtonComponent },
  name: "AboutUsBlock",
  props: { aboutUsObject: Object },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.about-us-section {
  // background-color: black;
  //   background-image: url("../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  background-image: url("../assets/business-people-working-together-on-project-and-5FHSKBL.jpg");
  background-size: 55% auto;
  background-repeat: no-repeat;
  background-position: left top;

  .about-us-text-section {
    color: white;
    padding: 200px 50px;
    text-align: left;
    .about-us-title {
      font-size: 38px;
    }
    .about-us-text-description {
      font-size: 14px;
      padding-top: 20px;
      color: $light-text-color;
    }
  }
}
.call-to-action {
  background: linear-gradient(
    90deg,
    $accent-color 0%,
    $accent-color 50%,
    $bg-dark 53%,
    $bg-dark 100%
  );
  .call-to-action-content {
    background-color: $accent-color;
    text-align: end;
    position: relative;
    .call-to-action-title {
      padding: 100px 20px;
    }
    .call-to-action-description {
      font-size: 14px;
      padding: 100px 20px;
      text-align: left;
      color: $light-text-color;
    }
    .call-to-action-button {
      position: absolute;
      bottom: 0;
      right: 0;
      background-color: $primary-color;
      color: white;
    }
  }
}
</style>