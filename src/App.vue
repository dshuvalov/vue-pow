<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <button @click="click">⬆︎</button>
    <input v-model="exps">
    <Degs :options="options"/>
  </div>
</template>

<script>
import Degs from "./components/Degs.vue";

export default {
  name: "app",
  components: {
    Degs
  },
  data() {
    return {
      exps: 5
    };
  },
  computed: {
    options: function() {
      return Array.from({ length: this.exps }, (v, i) => 10 + i);
    }
  },
  methods: {
    click: function() {
      this.exps = this.exps + 1;
    }
  }
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
