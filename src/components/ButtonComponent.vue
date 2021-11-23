<template>
  <a class="btn btn-success custom-button" :href="href">{{ text }}</a>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: { text: String, href: String },
};
</script>

<style lang="scss" scoped>
.custom-button {
  border-radius: 0;
  text-transform: uppercase;
  margin-right: 0;
}
</style>