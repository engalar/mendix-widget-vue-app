<template>
  <h1>{{ name }}</h1>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <button v-on:click="onClick()">点我</button>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data: () => {
    return {};
  },
  props: {
    name: {
      type: String,
      default: "张三",
    },
  },
  methods: {
    onClick() {
      let data = {
        cityname: "some value param",
      };
      this.$emit("showCityName", data);
    },
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
