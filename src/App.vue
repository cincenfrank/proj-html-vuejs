<template>
  <div id="app">
    <HeaderComponent :headerData="pageData.header"></HeaderComponent>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
export default {
  name: "App",
  components: { HeaderComponent },
  data() {
    return {
      pageData: {
        header: {
          backgroundImage:
            "../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg",
          nav: {
            logo: {
              href: "#",
              image: require("@/assets/logotype.png"),
              alt: "PHLOX logo",
            },
            links: [
              { text: "home", href: "#" },
              { text: "about", href: "#" },
              { text: "projects", href: "#" },
              { text: "services", href: "#" },
              { text: "blog", href: "#" },
              { text: "contact", href: "#" },
            ],
          },
          jumbo: {
            mainTitle: "the best business consulting",
            catchFrase: "always the best way you need it",
            button: { text: "read more", href: "#" },
            videoHref: "#",
          },
        },
        main: {
          servicesBlock: {
            title: "our consultants can help you",
            services: [
              {
                title: "statistical consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "",
              },
              {
                title: "digital consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "",
              },
              {
                title: "banking consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "",
              },
              {
                title: "enterprise consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "",
              },
            ],
          },
        },
      },
    };
  },
};
</script>

<style lang="scss">
#app {
  // font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  // margin-top: 60px;
}
</style>
