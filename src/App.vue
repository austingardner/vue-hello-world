<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <div>topCount: {{ topCount }}</div>
    <HelloWorld msg="Hello Vue in CodeSandbox!" />
    <MyInput
      v-on:topcountup="increment"
      :topCount="topCount"
      placeholder="I am a placeholder"
    />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import MyInput from "./components/MyInput";
export default {
  name: "App",
  components: {
    HelloWorld,
    MyInput,
  },
  data() {
    return {
      topCount: 0,
    };
  },
  methods: {
    increment() {
      this.topCount++;
    },
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
</style>
