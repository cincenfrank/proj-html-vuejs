<template>
  <section class="container">
    <div class="services-block">
      <TitleComponent
        class="text-start"
        :priority="4"
        :text="servicesObject.title"
      ></TitleComponent>
      <div class="row row-cols-2 gap-2 justify-content-between">
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
  </section>
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
.services-block {
  padding: 100px;
}
</style>