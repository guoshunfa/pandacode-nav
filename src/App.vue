<template>
  <div id="app">
    <el-container>
      <el-header>
        <Header id="header"></Header>
      </el-header>

      <el-container>
        <el-main class="main">
          <Search class="search"></Search>
          <Collect class="collect"></Collect>
          <Tool class="tool"></Tool>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import Header from "./views/Header.vue";
import Collect from "./views/Collect.vue";
import Tool from "./views/Tool.vue";
import Search from "./views/Search.vue";

export default {
  name: "app",
  components: {
    Header,
    Search,
    Collect,
    Tool,
  },
};
</script>
<style>
html,
body {
  height: 100%;
}
body {
  margin: 0;
  background: #8676e4;
}
</style>
<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
}
.header {
  height: 10%;
}
.main {
  height: 75%;
}

.search {
  height: 20%;
  widows: 30%;
  margin: 5% 30% 5% 30%;
}
.collect {
  width: 75%;
  float: left;
  height: 65%;
}
.tool {
  width: 20%;
  float: right;
  height: 65%;
}
</style>
