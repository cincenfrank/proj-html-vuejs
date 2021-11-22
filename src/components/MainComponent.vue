<template>
  <main>
    <ServicesBlock :servicesObject="mainObject.servicesBlock"></ServicesBlock>
  </main>
</template>

<script>
import ServicesBlock from "./ServicesBlock.vue";
export default {
  components: { ServicesBlock },
  name: "MainComponent",
  props: { mainObject: Object },
};
</script>

<style lang="scss" scoped>
</style>