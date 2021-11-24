<template>
  <div class="bg-white overflow-hidden">
    <section class="container">
      <div class="services-block">
        <div class="d-flex align-items-center service-row">
          <TitleComponent
            class="text-start service-title"
            :priority="4"
            :text="servicesObject.title"
          ></TitleComponent>
          <div class="service-title-line"></div>
        </div>
        <div class="overflow-hidden">
          <div class="row row-cols-2 gap-2 gy-5 justify-content-between">
            <div
              class="col-5"
              v-for="(service, i) in servicesObject.services"
              :key="i + '-services'"
            >
              <ServiceCard
                :title="service.title"
                :description="service.description"
                :iconClass="service.icon"
              ></ServiceCard>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import ServiceCard from "./ServiceCard.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { ServiceCard, TitleComponent },
  name: "ServicesBlock",
  props: { servicesObject: Object },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.services-block {
  padding: 100px;
  .service-row {
    margin-bottom: 100px;
    .service-title {
      // margin-bottom: 100px;
      flex-shrink: 0;
      margin-right: 50px;
    }
    .service-title-line {
      border-bottom: 2px solid $accent-color;
      flex-grow: 1;
      margin-right: -100%;
    }
  }
}
</style>