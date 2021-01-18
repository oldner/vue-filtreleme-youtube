<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <UserList :list="list"> </UserList>
</template>

<script>
import UserList from "@/components/UserList.vue";
export default {
  name: "App",
  components: {
    UserList,
  },
  data() {
    return {
      list: ["ali", "ahmet", "mehmet", "cemal", "süreyya", "ibrahim"],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
