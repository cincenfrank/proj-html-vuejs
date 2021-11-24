<template>
  <nav class="footer-navbar d-flex align-items-center justify-content-between">
    <img
      width="80"
      :src="footerNavObject.logo.image"
      :alt="footerNavObject.logo.alt"
    />
    <ul class="links-list">
      <li
        class="links-item"
        v-for="(item, i) in footerNavObject.links"
        :key="i + '-footer-link'"
      >
        <a :href="item.href">{{ item.text }}</a>
      </li>
    </ul>
    <ul class="social-list">
      <li
        class="social-item"
        v-for="(social, i) in footerNavObject.social"
        :key="i + '-footer-social'"
      >
        <a :href="social.href"><i class="fab" :class="social.icon"></i></a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "FooterNavbar",
  props: { footerNavObject: Object },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.footer-navbar {
  margin-bottom: 50px;
  .links-list,
  .social-list {
    list-style: none;
    display: flex;
    margin: 0;
  }
  .links-item {
    padding: 10px;
    a {
      text-decoration: none;
      color: $secondary-color;
    }
    &:hover {
      a {
        color: white;
      }
    }
  }
  .social-item {
    padding: 10px;
    a {
      text-decoration: none;
      color: white;
    }
  }
}
</style>