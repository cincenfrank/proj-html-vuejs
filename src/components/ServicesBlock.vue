<template>
  <section>
    <ContextTitle text="xxx"></ContextTitle>
  </section>
</template>

<script>
import ContextTitle from "./ContextTitle.vue";
export default {
  components: { ContextTitle },
  name: "ServicesBlock",
  props: { servicesObject: Object },
};
</script>

<style lang="scss" scoped>
</style>