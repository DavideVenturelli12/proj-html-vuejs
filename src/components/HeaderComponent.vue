<template>
  <header>
    <!--Navbar-->
    <div class="nav-section">
      <img src="../assets/logo.png" alt="logo" />
      <div class="nav-links">
        <ul>
          <li v-for="item in nav" :key="item">
            <a href="#">{{ item }}</a>
          </li>
        </ul>
        <button><i class="fa-solid fa-magnifying-glass"></i></button>
      </div>
    </div>
    <!--Jumbotron-->
    <div id="jumbotron">
      <h1>Tech Forum!</h1>
      <p>Discuss all the latest technology news and trends</p>
      <button>GET AVADA NOW! <i class="fa-solid fa-chevron-right"></i></button>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: {
    nav: Array,
  },
};
</script>

<style lang="scss" scoped>
.nav-section {
  padding: 0 15%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: hsl(188deg 67% 45%);
  img {
    height: 45px;
    margin: 10px 0;
  }
  .nav-links {
    display: flex;
    ul {
      list-style: none;
      li {
        display: inline-block;
        padding: 5px 0;
        a {
          text-decoration: none;
          color: white;
          font-size: 14px;
          font-weight: 600;
          margin: 0 15px;
          padding: 10px;
        }
        a:hover {
          background-color: black;
        }
      }
    }
  }

  button {
    background-color: transparent;
    border: 0;
    color: white;
    cursor: pointer;
    margin-left: 15px;
    i {
      font-size: 14px;
    }
  }
  button:active {
    transform: scale(0.9);
  }
}
#jumbotron {
  padding: 10% 15%;
  color: white;
  background-image: url(../assets/home_slider_bg.jpg);
  background-position: center;
  background-size: cover;
  h1 {
    font-size: 100px;
  }
  p {
    margin: 20px 0;
    color: lightgrey;
  }
  button {
    background-color: hsl(188deg 67% 45%);
    padding: 10px 20px;
    border: 0;
    color: white;
    font-weight: 600;
    cursor: pointer;
  }
  button:active {
    transform: scale(0.9);
  }
}
</style>