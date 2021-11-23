<template>
  <main>
    <ServicesBlock :servicesObject="mainObject.servicesBlock"></ServicesBlock>
    <AboutUsBlock :aboutUsObject="mainObject.aboutUsBlock"></AboutUsBlock>
  </main>
</template>

<script>
import AboutUsBlock from "./AboutUsBlock.vue";
import ServicesBlock from "./ServicesBlock.vue";
export default {
  components: { ServicesBlock, AboutUsBlock },
  name: "MainComponent",
  props: { mainObject: Object },
};
</script>

<style lang="scss" scoped>
</style>