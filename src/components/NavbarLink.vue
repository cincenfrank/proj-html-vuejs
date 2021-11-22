<template>
  <a class="nav-link" :class="isActive ? 'active' : ''" :href="href">{{
    text
  }}</a>
</template>

<script>
export default {
  name: "NavbarLink",
  props: {
    isActive: Boolean,
    // isDisabled: Boolean,
    href: String,
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.nav-link {
  text-transform: uppercase;
}
</style>