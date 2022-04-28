<template>
  <div id="app">
    <HeaderComponent :nav="nav" />
    <MainComponent :principalNews="principalNews" />
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
          option1: "Lorem ipsum dolor",
          option2:
            "Minus, nemo magnam magni laudantium illum labore mollitia esse quos sit.",
          option3:
            "Fusce leo nibh, feugiat ac ullamcorper id, placerat ut enim.",
          option4: "Proin ultrices lacinia gravida.",
        },
        {
          voice: "RECENT TOPICS",
          option1:
            "Mauris dictum quam arcu, ullamcorper commodo est varius at.",
          option2: "Cras placerat consequat erat.",
          option3:
            "Donec vitae arcu sit amet augue ultricies vehicula faucibus sit amet neque.",
          option4:
            "Quisque vitae enim non arcu mattis condimentum sit amet in ipsum.",
        },
        {
          voice: "LATEST REPLIES",
          option1:
            "Etiam dictum nulla at metus eleifend, ac ultrices nisl molestie.",
          option2: "Nulla viverra maximus tellus vitae placerat.",
          option3: "Phasellus consectetur gravida ex non lobortis.",
          option4:
            "Donec eleifend leo ut ex blandit, at condimentum odio ornare.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/style/general";
</style>
