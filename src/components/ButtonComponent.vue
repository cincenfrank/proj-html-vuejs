<template>
  <button class="btn btn-success">{{ text }}</button>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: { text: String },
};
</script>

<style lang="scss" scoped>
</style>