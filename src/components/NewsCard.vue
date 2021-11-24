<template>
  <div class="news-card">
    <img :src="imageSrc" :alt="imageAlt" />
    <div class="text-block">
      <div>
        <span class="news-date">{{ date }}</span>
        <span class="news-author">by {{ author }}</span>
      </div>

      <h5 class="news-title">{{ title }}</h5>
      <p class="news-preview">{{ preview }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewsCard",
  props: {
    imageSrc: String,
    imageAlt: String,
    date: String,
    author: String,
    title: String,
    preview: String,
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.news-card {
  width: 100%;
  //   padding-bottom: 100px;
  background-color: white;
  position: relative;
  margin-bottom: 25%;
  img {
    height: 100%;
    width: 100%;
  }
  .text-block {
    cursor: pointer;
    position: absolute;
    transform: translateY(30%);
    width: 75%;
    background-color: white;
    right: 0;
    bottom: 0;
    text-align: left;
    padding: 30px 50px;
    .news-date,
    .news-author {
      font-size: 14px;
      margin-right: 20px;
      color: $primary-color;
    }
    .news-title {
      padding: 20px 0;
      font-weight: bold;
      text-transform: capitalize;
    }
    .news-preview {
      font-size: 14px;
    }
  }
}
</style>