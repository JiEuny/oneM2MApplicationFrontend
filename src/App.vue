<template>
  <div id="app">
    <el-container>
      <el-aside class="header">
        <Header />
      </el-aside>
    </el-container>

    <router-view class="el-main" />
  </div>
</template>

<script>
import Header from "./components/Header";

export default {
  name: "App",
  components: {
    Header
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.el-aside {
  position: relative;
  /* background: #545c64; */
  color: white;
  min-width: 100%;
  min-height: 200px;
  background: #3b4346;
  border-bottom: solid 1px #272d30;
  box-shadow: inset 0px -1px 0px 0px #51575a;
  text-shadow: -1px -1px 1px rgba(0, 0, 0, 0.75);
}

.el-menu {
  border-right: 0 !important;
}

.el-main {
  background: #c5cfda;
  padding: 45px 0 45px 0;
}

.header a {
  color: #fff;
  padding-right: 5px;
  text-decoration: none;
}
</style>
