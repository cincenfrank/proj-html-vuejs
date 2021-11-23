<template>
  <div id="app">
    <HeaderComponent :headerData="pageData.header"></HeaderComponent>
    <MainComponent :mainObject="pageData.main"></MainComponent>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";
export default {
  name: "App",
  components: { HeaderComponent, MainComponent },
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
                icon: "fa-chart-line",
              },
              {
                title: "digital consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "fa-bullhorn",
              },
              {
                title: "banking consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "fa-wallet",
              },
              {
                title: "enterprise consulting",
                description:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                icon: "fa-bullseye",
              },
            ],
          },
          aboutUsBlock: {
            contextTitle: "about us",
            title: "we make your strategy work",
            description:
              "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a thousand unknown are noticed when I hear the buzz of the little world among the stalks, and grow familiar indescribable forms of the insects. And flies, then I feel the presence of Almighty",
            callToAction: {
              text: "we help to deliver the business case",
              description:
                "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a thousand unknown",
              button: { text: "get started", href: "#" },
            },
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
