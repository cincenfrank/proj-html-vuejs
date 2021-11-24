<template>
  <footer class="footer">
    <div class="container">
      <FooterNavbar :footerNavObject="footerObject.nav"></FooterNavbar>
      <div class="footer-divider"></div>
      <div class="d-flex justify-content-between align-items-end">
        <div class="d-flex flex-column align-items-start">
          <a :href="footerObject.credits.terms.href">{{
            footerObject.credits.terms.text
          }}</a>
          <a :href="footerObject.credits.privacy.href">{{
            footerObject.credits.privacy.text
          }}</a>
        </div>
        <p class="m-0">{{ footerObject.credits.copyright }}</p>
      </div>
    </div>
  </footer>
</template>

<script>
import FooterNavbar from "./FooterNavbar.vue";
export default {
  components: { FooterNavbar },
  name: "FooterComponent",
  props: { footerObject: Object },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.footer {
  padding: 50px 0;
  background-color: $bg-dark;
  color: $secondary-color;
  font-size: 12px;
  text-transform: capitalize;
  a {
    color: $secondary-color;
    text-decoration: none;
  }
  .footer-divider {
    width: 100%;
    border-bottom: 2px solid $secondary-color;
    margin: 30px 0;
  }
}
</style>