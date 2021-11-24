<template>
  <h1 v-if="priority === 1" class="title main">{{ text }}</h1>
  <h2 v-else-if="priority === 2" class="title">{{ text }}</h2>
  <h3 v-else-if="priority === 3" class="title">{{ text }}</h3>
  <h4 v-else-if="priority === 4" class="title">{{ text }}</h4>
  <h5 v-else-if="priority === 5" class="title">{{ text }}</h5>
</template>

<script>
export default {
  name: "TitleComponent",
  props: {
    text: String,
    priority: { default: 1 },
  },
};
</script>

<style lang="scss" scoped>
.title {
  text-transform: uppercase;
  text-align: left;
  font-weight: bold;
  &.main {
    font-size: 80px;
    color: white;
  }
}
</style>