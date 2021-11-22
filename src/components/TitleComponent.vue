<template>
  <h1 v-if="priority === 1" class="title">{{ text }}</h1>
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

<style>
* {
  text-transform: uppercase;
}
.title {
  font-size: 80px;
  color: white;
}
</style>