<template>
  <a
    class="nav-link"
    :class="isActive ? 'active' : ''"
    :href="href"
    @click="onClick"
    >{{ text }}</a
  >
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
  methods: {
    onClick() {
      this.$emit("linkClicked");
    },
  },
};
</script>

<style lang="scss" scoped>
.nav-link {
  text-transform: uppercase;
  font-size: 11px;
  padding: 20px 50px;

  border-top: 1px solid transparent;
  &.active {
    font-weight: bold;
    border-top: 1px solid white;
  }
}
</style>