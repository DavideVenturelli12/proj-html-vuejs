<template>
  <main>
    <!--Descrizione-->
    <div class="description-section">
      <h3>AVADA FORUM IS THE PLACE TO BE</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus ab
        placeat ducimus doloremque fugiat facilis amet saepe similique neque
        earum eligendi perferendis minima, qui quia voluptatum beatae, dolores
        eveniet voluptates!
      </p>
    </div>
    <!--Titolo-->
    <div class="title-section">
      <h3>PHASELLUS EGET METUS</h3>
      <h2>All the latest news</h2>
      <div class="bar"></div>
    </div>
    <!--prima Sezione news-->
    <div class="news-section">
      <div class="news" v-for="(item, index) in news1" :key="index">
        <img :src="item.img" :alt="item.image" />
        <h4>{{ item.title }}</h4>
        <p>
          {{ item.date }}<strong>{{ item.comments }}</strong>
        </p>
        <p class="preview">{{ item.preview }}</p>
      </div>
    </div>
    <!--sezione fetured article-->
    <div class="featured-article">
      <h3>FEATURED ARTICLE</h3>
      <h2>Cras malesuada et orci eget pharetra</h2>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas sint
        facilis obcaecati eveniet fugiat nemo porro rem veniam sed. Consectetur
        dolorem fuga alias ipsum laudantium temporibus labore perspiciatis eum
        dolores.
      </p>
      <button>READ MORE <i class="fa-solid fa-chevron-right"></i></button>
    </div>
    <!--seconda sezione news-->
    <div class="news-section">
      <div class="news" v-for="(item, index) in news2" :key="index">
        <img :src="item.img" :alt="item.image" />
        <h4>{{ item.title }}</h4>
        <p>
          {{ item.date }}<strong>{{ item.comments }}</strong>
        </p>
        <p class="preview">{{ item.preview }}</p>
      </div>
    </div>
    <!--Sezione tutorial e guide-->
    <div class="tutorial-section">
      <div class="reviewed-product">
        <h3>REVIEWED PRODUCT</h3>
        <h2>Mauris viverra atisan ipsum eget felis prims eficitur varius</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas sint
          facilis obcaecati eveniet fugiat nemo porro rem veniam sed.
          Consectetur dolorem fuga alias ipsum laudantium temporibus labore
          perspiciatis eum dolores.
        </p>
        <button>READ MORE <i class="fa-solid fa-chevron-right"></i></button>
      </div>
      <div class="tutorial">
        <div>
          <h3>Tutorials e guides</h3>
          <div class="bar"></div>
        </div>
        <div>
          <div class="guides" v-for="(item, index) in tutorial" :key="index">
            <img :src="item.img" :alt="item.image" />
            <div>
              <h4>{{ item.title }}</h4>
              <p>
                {{ item.date }}<strong>{{ item.commnets }}</strong>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--link al blog-->
    <div id="go-to">
      <h3>
        <a href="#"
          >READ OUR BLOG <i class="fa-solid fa-arrow-right-long"></i
        ></a>
      </h3>
    </div>
    <!--link ai forum-->
    <div class="forum-section">
      <div class="title-section">
        <h3>PHASELLUS EGET METUS</h3>
        <h2>forum section</h2>
        <div class="bar"></div>
      </div>
    </div>
    <div class="forum-link">
      <div v-for="(item, index) in forum" :key="index">
        <i id="icon" :class="item.icon"></i>
        <a href="#">
          <h3>{{ item.title }}</h3>
        </a>
      </div>
    </div>
    <!--Link al tuo forum-->
    <div id="go-to">
      <h3>
        <a href="#"
          >GO TO YOUR FORUM <i class="fa-solid fa-arrow-right-long"></i
        ></a>
      </h3>
    </div>
    <!--Iscrizione-->
    <div class="sign-up">
      <h1>Hey! Join to our community</h1>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Qui tempora
        modi recusandae quisquam sed corporis vel.
      </p>
      <button>SIGN UP <i class="fa-solid fa-chevron-right"></i></button>
    </div>
    <!--Newsletter-->
    <div class="newsletter">
      <h3>Subscibe to our Newsletter</h3>
      <input type="text" placeholder="Insert your email*" />
      <button>SEND</button>
    </div>
  </main>
</template>

<script>
import news1 from "../assets/data/mainNewsData1.js";
import news2 from "../assets/data/mainNewsData2.js";
import tutorial from "../assets/data/tutorialData.js";
import forum from "../assets/data/forumLinkData.js";

export default {
  name: "MainComponent",
  data() {
    return {
      news1,
      news2,
      tutorial,
      forum,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/main";
</style>