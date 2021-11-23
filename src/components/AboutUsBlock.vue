<template>
  <div>
    <section class="about-us-section">
      <div class="container">
        <div class="row justify-content-end">
          <div class="col-5">
            <div class="about-us-text-section">
              <ContextTitle :text="aboutUsObject.contextTitle"></ContextTitle>
              <TitleComponent
                :priority="2"
                :text="aboutUsObject.title"
              ></TitleComponent>
              <p>{{ aboutUsObject.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="call-to-action">
      <div class="call-to-action-content container">
        <div class="row justify-content-evenly">
          <div class="col-3">
            <TitleComponent
              :priority="3"
              :text="aboutUsObject.callToAction.text"
            ></TitleComponent>
          </div>
          <div class="col-3">
            <p>
              {{ aboutUsObject.callToAction.description }}
            </p>
          </div>
        </div>
        <ButtonComponent
          class=""
          :text="aboutUsObject.callToAction.button.text"
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
.about-us-section {
  background-color: black;
  //   background-image: url("../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  background-image: url("../assets/business-people-working-together-on-project-and-5FHSKBL.jpg");
  background-size: 55% 100%;
  background-repeat: no-repeat;
  background-position: left top;

  .about-us-text-section {
    color: white;
    padding: 200px 50px;
    text-align: left;
  }
}
.call-to-action {
  .call-to-action-content {
    background-color: yellowgreen;
    text-align: end;
  }
}
</style>