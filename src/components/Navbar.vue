<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="container">
      <a class="navbar-brand" :href="navbarObject.logo.href">
        <img
          :src="navbarObject.logo.image"
          :alt="navbarObject.logo.alt"
          width="80"
        />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        x
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li
            class="nav-item"
            v-for="(link, i) in navbarObject.links"
            :key="i + 'nav-link'"
          >
            <NavbarLink
              isActive="false"
              :href="link.href"
              :text="link.text"
            ></NavbarLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import NavbarLink from "./NavbarLink.vue";
export default {
  components: { NavbarLink },
  name: "Navbar",
  props: { navbarObject: Object },
};
</script>

<style>
</style>