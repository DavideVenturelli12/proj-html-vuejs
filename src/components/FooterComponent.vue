<template>
  <footer>
    <div class="top-footer">
      <div id="footer-description">
        <h3>AVADA THECH FORUM</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio aperiam
          iste dolorum assumenda quibusdam cum nisi harum, laudantium ipsa
          ducimus hic quidem, placeat ab rem ex debitis eligendi nobis
          reiciendis.
        </p>
      </div>
      <div id="footer-info" v-for="item in footerInfo" :key="item">
        <ul>
          <li>
            <h3>{{ item.voice }}</h3>
            <p>
              <a href="#">{{ item.option1 }}</a>
            </p>
            <p>
              <a href="#">{{ item.option2 }}</a>
            </p>
            <p>
              <a href="#">{{ item.option2 }}</a>
            </p>
          </li>
        </ul>
      </div>
    </div>
    <div class="bottom-footer">
      <div id="copyright-social">
        <div>
          <p>
            <i class="fa-regular fa-copyright"></i> Copyright 2012-2022 | Avada
            Theme by <strong>Theme Fusion</strong> | All Rights Reserved |
            Powered by
            <strong>WorldPress</strong>
          </p>
        </div>
        <div>
          <i class="fa-brands fa-facebook-f fb social"></i>
          <i class="fa-brands fa-twitter tw social"></i>
          <i class="fa-brands fa-instagram ig social"></i>
          <i class="fa-brands fa-youtube yt social"></i>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  props: {
    footerInfo: Array,
  },
};
</script>

<style lang="scss" scoped>
.top-footer {
  display: flex;
  padding: 70px 15%;
  #footer-description,
  #footer-info {
    padding: 0 15px;
  }
  #footer-description {
    width: calc(100% / 4);
    h3 {
      margin-bottom: 30px;
    }
    p {
      font-size: 14px;
      line-height: 25px;
    }
  }
  #footer-info {
    display: flex;
    width: calc(100% / 4);
    h3 {
      margin-bottom: 20px;
    }
    ul {
      list-style: none;
    }
    p {
      padding: 10px 0;
      border-bottom: 1px solid lightgray;
      font-size: 13px;
      font-weight: 600;
      a {
        text-decoration: none;
        line-height: 25px;
        color: black;
      }
    }
  }
}
.bottom-footer {
  border-top: 1px solid lightgray;
  #copyright-social {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 30px 15%;
    p {
      font-size: 11px;
    }
    .social {
      height: 40px;
      width: 40px;
      text-align: center;
      line-height: 40px;
      vertical-align: middle;
      border-radius: 50%;
      color: white;
      font-size: 20px;
      margin-left: 10px;
    }
    .fb {
      background-color: hsl(221deg 43% 42%);
    }
    .tw {
      background-color: hsl(206deg 82% 63%);
    }
    .ig {
      background-color: hsl(207deg 42% 43%);
    }
    .yt {
      background-color: hsl(0deg 74% 46%);
    }
  }
}
</style>