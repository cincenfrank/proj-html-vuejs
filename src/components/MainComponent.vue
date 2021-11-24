<template>
  <main>
    <ServicesBlock :servicesObject="mainObject.servicesBlock"></ServicesBlock>
    <AboutUsBlock :aboutUsObject="mainObject.aboutUsBlock"></AboutUsBlock>
    <ProjectBlock :projectObject="mainObject.projectBlock"></ProjectBlock>
    <TestimonialBlock
      :testimonialObject="mainObject.testimonialBlock"
    ></TestimonialBlock>
    <BlogBlock :blockObject="mainObject.blogBlock"></BlogBlock>
    <WorkBlock :workObject="mainObject.workBlock"></WorkBlock>
  </main>
</template>

<script>
import AboutUsBlock from "./AboutUsBlock.vue";
import BlogBlock from "./BlogBlock.vue";
import ProjectBlock from "./ProjectBlock.vue";
import ServicesBlock from "./ServicesBlock.vue";
import TestimonialBlock from "./TestimonialBlock.vue";
import WorkBlock from "./WorkBlock.vue";
export default {
  components: {
    ServicesBlock,
    AboutUsBlock,
    ProjectBlock,
    TestimonialBlock,
    BlogBlock,
    WorkBlock,
  },
  name: "MainComponent",
  props: { mainObject: Object },
};
</script>

<style lang="scss" scoped>
main {
  // background-color: darkblue;
}
</style>