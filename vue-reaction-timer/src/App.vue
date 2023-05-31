<template>
  <div>
    <h1>Reaction TImer</h1>
    <button @click="start" :disabled="isPlaying">Play</button>
    <Game v-if="isPlaying" :delay="delay" />
  </div>
</template>


<script>
import Game from "./components/Game.vue";

export default {
  name: "App",
  components: { Game },
  data() {
    return {
      isPlaying: false,
      delay: null,
    };
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000;
      this.isPlaying = true;
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
