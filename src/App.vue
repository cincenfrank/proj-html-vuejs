<template>
  <div id="app">
    <HeaderComponent :headerData="pageData.header"></HeaderComponent>
    <MainComponent :mainObject="pageData.main"></MainComponent>
    <FooterComponent :footerObject="pageData.footer"></FooterComponent>
    <div
      class="
        chat-icon
        bg-info
        p-3
        rounded-circle
        d-inline-block
        position-fixed
        bottom-0
        end-0
        m-5
      "
    >
      <i class="far fa-comment"></i>
    </div>
  </div>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";
export default {
  name: "App",
  components: { HeaderComponent, MainComponent, FooterComponent },
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
          projectBlock: {
            contextTitle: "project",
            slider: {
              title: "our expert trusted consultants help clients",
              itemList: [
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg"),
                  alt: "desc",
                },
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/DRY-1-790x592.jpg"),
                  alt: "desc",
                },
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/z1el4c4p-790x592.jpg"),
                  alt: "desc",
                },
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg"),
                  alt: "desc",
                },
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/DRY-1-790x592.jpg"),
                  alt: "desc",
                },
                {
                  title: "purinky products",
                  category: "uncategorized",
                  image: require("@/assets/z1el4c4p-790x592.jpg"),
                  alt: "desc",
                },
              ],
            },
          },
          testimonialBlock: {
            contextTitle: "testimonial",
            title: "what's the customer say about our work",
            testimonialsList: [
              {
                name: "vera duncan",
                company: "amazon inc.",
                review:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a thousand unknown are noticed when I hear the buzz of the little",
                img: require("@/assets/oliver-ragfelt-488196-2.jpg"),
              },
              {
                name: "vera duncan",
                company: "amazon inc.",
                review:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a thousand unknown are noticed when I hear the buzz of the little",
                img: require("@/assets/oliver-ragfelt-488196-2.jpg"),
              },
              {
                name: "vera duncan",
                company: "amazon inc.",
                review:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a thousand unknown are noticed when I hear the buzz of the little",
                img: require("@/assets/oliver-ragfelt-488196-2.jpg"),
              },
            ],
          },
          blogBlock: {
            contextTitle: "blog",
            title: "the recent news you must read it",
            button: { text: "view all", href: "#" },
            newsList: [
              {
                image: require("@/assets/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg"),
                title: "canadian consulting firm acquired by UK Giant",
                preview:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                date: "July 4, 2019",
                author: "paul",
              },
              {
                image: require("@/assets/business-people-working-together-on-project-and-5FHSKBL-1390.jpg"),
                title: "canadian consulting firm acquired by UK Giant",
                preview:
                  "When, while lovely valley teems with vapour around meridian sun strikes the upper impenetrable foliage of my trees and but a",
                date: "July 4, 2019",
                author: "paul",
              },
            ],
          },
          workBlock: {
            title: "lets talk about work",
            description:
              "a wonderful serenity has taken possession Far far away, behind the word mountains",
            button: { text: "get started", href: "#" },
          },
        },
        footer: {
          nav: {
            logo: {
              href: "#",
              image: require("@/assets/logotype-2-300x50.png"),
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
            social: [
              {
                icon: "fa-instagram",
                href: "#",
              },
              {
                icon: "fa-linkedin-in",
                href: "#",
              },
              {
                icon: "fa-facebook-f",
                href: "#",
              },
              {
                icon: "fa-twitter",
                href: "#",
              },
            ],
          },
          credits: {
            terms: { text: "terms of use", href: "#" },
            privacy: { text: "terms environmental policy", href: "#" },
            copyright: "copyright c 2020 phlox consulting all rights reserved.",
          },
        },
      },
    };
  },
};
</script>

<style lang="scss">
@import "@/styles/variables.scss";
#app {
  font-family: "aktiv-grotesk-std", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: $bg-dark;
  // margin-top: 60px;

  .chat-icon {
    cursor: pointer;
    &:hover {
    }
  }
}
</style>
