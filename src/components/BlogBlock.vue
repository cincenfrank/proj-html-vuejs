<template>
  <div class="container blog-block">
    <ContextTitle :text="blockObject.contextTitle"></ContextTitle>
    <div class="d-flex justify-content-between align-items-center pb-5">
      <TitleComponent
        :priority="3"
        :text="blockObject.title"
        class="text-white m-0"
      ></TitleComponent>
      <ButtonComponent
        :text="blockObject.button.text"
        :href="blockObject.button.href"
      ></ButtonComponent>
    </div>

    <div class="row">
      <div
        class="col-6"
        v-for="(news, i) in blockObject.newsList"
        :key="i + '-news'"
      >
        <NewsCard
          :author="news.author"
          :date="news.date"
          :imageSrc="news.image"
          :preview="news.preview"
          :title="news.title"
          :imageAlt="news.title + ' image'"
        ></NewsCard>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
import ContextTitle from "./ContextTitle.vue";
import NewsCard from "./NewsCard.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { ContextTitle, TitleComponent, ButtonComponent, NewsCard },
  name: "BlogBlock",
  props: { blockObject: Object },
};
</script>

<style lang="scss" scoped>
.blog-block {
  padding-bottom: 200px;
}
</style>