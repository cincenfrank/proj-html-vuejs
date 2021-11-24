<template>
  <div class="jumbo container">
    <div class="row">
      <div class="col-5">
        <ContextTitle :text="jumboObject.catchFrase"></ContextTitle>
        <TitleComponent
          :priority="1"
          :text="jumboObject.mainTitle"
        ></TitleComponent>
        <div class="d-flex gap-4 align-items-center">
          <ButtonComponent
            :text="jumboObject.button.text"
            :href="jumboObject.button.href"
          ></ButtonComponent>
          <PlayButton class=""></PlayButton>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
import ContextTitle from "./ContextTitle.vue";
import PlayButton from "./PlayButton.vue";
import TitleComponent from "./TitleComponent.vue";
export default {
  components: { ContextTitle, TitleComponent, ButtonComponent, PlayButton },
  name: "JumboHeader",
  props: { jumboObject: Object },
};
</script>

<style>
.jumbo {
  text-align: left;
  padding: 200px 0;
}
</style>