<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <button @click="toggleSmartApply">
    {{ showSmartApply ? "Hide" : "Show" }} Smart Apply
  </button>

  <div v-if="showSmartApply" class="smart-apply" style="">
    <smart-apply />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      showSmartApply: false, // State variable to track visibility
    };
  },
  methods: {
    toggleSmartApply() {
      this.showSmartApply = !this.showSmartApply;
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
.smart-apply {
  width: 30%;
  border: 1px solid black;
  background-color: white;
  position: absolute;
  padding: 10px;
  top: 0;
  left: 0;
  right: 0;
  margin: 0;
}
</style>
