<template>
  <header>
    <Navbar :navbarObject="headerData.nav"></Navbar>
    <JumboHeader :jumboObject="headerData.jumbo"></JumboHeader>
  </header>
</template>

<script>
import JumboHeader from "./JumboHeader.vue";
import Navbar from "./Navbar.vue";
export default {
  components: { Navbar, JumboHeader },
  name: "HeaderComponent",
  props: { headerData: Object },
};
</script>

<style lang="scss" scoped>
header {
  background-color: black;
  background-image: url("../assets/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  background-size: 66%;
  background-repeat: no-repeat;
  background-position-x: right;
  background-position-y: top;
  //   padding: 10px;
}
</style>