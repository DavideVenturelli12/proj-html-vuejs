<template>
  <div id="app">
    <HeaderComponent :nav="nav" />
    <MainComponent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
  data() {
    return {
      nav: [
        "Home",
        "Apple",
        "Microsoft",
        "Android",
        "Forums",
        "Contact us",
        "Join us",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/style/general";
</style>
