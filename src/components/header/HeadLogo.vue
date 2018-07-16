<template>
  <div class="logo-container">
    <div class="head-logo">
      <a href="#">
        <img src="http://m.kugou.com/v3/static/images/index/logo.png">
      </a>
    </div>
    <div class="head-search" @click="searchRouter">
      <img src="http://m.kugou.com/v3/static/images/index/search.png">
    </div>
  </div>
</template>

<script type="es6">
export default {
  methods: {
    searchRouter() {
      this.$store.commit("showDetailPlayer", false);
      this.$router.push({ path: "/search" });
    }
  }
};
</script>

<style scoped>
.logo-container {
  padding: 10px;
  background-color: #2ca2f9;
  overflow: hidden;
  height: 51px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1050;
}
.head-logo {
  float: left;
  height: 100%;
}
.head-logo img {
  height: 100%;
}
.head-download {
  float: left;
  height: 31px;
  width: 25%;
  margin-left: 4%;
  line-height: 31px;
}
.head-download a {
  display: block;
  height: 100%;
  width: 100%;
  border: 1px solid #fff;
  text-align: center;
  color: #fff;
  border-radius: 5px;
}
.head-search {
  float: right;
  height: 31px;
  padding: 3px 0;
}
.head-search img {
  height: 100%;
}
</style>

