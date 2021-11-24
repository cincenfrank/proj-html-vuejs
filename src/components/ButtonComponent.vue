<template>
  <a class="btn custom-button" :href="href">{{ text }}</a>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: { text: String, href: String },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.custom-button {
  border-radius: 0;
  text-transform: uppercase;
  margin-right: 0;
  background-color: $accent-color;
  font-size: 12px;
  letter-spacing: 2px;
  padding: 15px 30px;
  border: 3px solid transparent;
  animation: all 0.3s;
  &:hover {
    border: 3px solid $bg-dark;
  }
}
</style>