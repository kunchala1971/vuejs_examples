<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Firtst VUEJs App" />
    <div>{{ name }}</div>
    <div v-text="name"></div>
    <div v-html="name_bold" v-bind:id="nameid"></div>
    <button v-bind:disabled="isDisabled" @click="handleClick">Click Me</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      name: "SrinivasaRao",
      name_bold:"<b>Kunchala SrinivasaRao</b>",
      nameid:111,
      isDisabled:false,
    };
  },
  components: {
    HelloWorld,
  },
  methods: {
    handleClick() {
      alert("Button was clicked!");
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
  margin-top: 20px;
}
</style>
