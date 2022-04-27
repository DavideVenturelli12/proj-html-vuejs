<template>
  <div id="app">
    <HeaderComponent :nav="nav" />
    <MainComponent />
    <FooterComponent :footerInfo="footerInfo" />
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
      footerInfo: [
        {
          voice: "POPULAR TOPICS",
          option1: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option2: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option3: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
        },
        {
          voice: "RECENT TOPICS",
          option1: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option2: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option3: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
        },
        {
          voice: "LATEST REPLIES",
          option1: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option2: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
          option3: "Lorem ipsum dolor sit amet consectetur adipisicing elit",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/style/general";
</style>
