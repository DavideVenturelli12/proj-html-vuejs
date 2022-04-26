<template>
  <header>
    <img src="../assets/logo.png" alt="logo" />
    <div class="nav-section">
      <ul>
        <li v-for="item in nav" :key="item">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
      <button><i class="fa-solid fa-magnifying-glass"></i></button>
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
header {
  display: flex;
  align-items: center;
  justify-content: space-around;
  background-color: hsl(188deg 67% 45%);
  img {
    height: 45px;
    margin: 10px 0;
  }
  .nav-section {
    display: flex;
    ul {
      list-style: none;
      li {
        display: inline-block;
        a {
          text-decoration: none;
          color: white;
          font-size: 14px;
          font-weight: 600;
          margin: 0 15px;
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
  }
}
</style>