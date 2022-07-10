<script>
import Sidebar from "./components/Sidebar.vue";
import silence from "./assets/silence.mp3";

export default {
  name: "App",
  data() {
    return {
      isPlayed: false,
    };
  },
  methods: {
    playMusic(id) {
      if (this.isPlayed) {
        document.getElementById(id).play();
        this.isPlayed = !this.isPlayed;
      } else {
        document.getElementById(id).pause();
        this.isPlayed = !this.isPlayed;
      }
    },
  },
  components: {
    Sidebar,
  },
};
</script>

<template>
  <audio id="playAudio" loop autoplay>
    <source src="./assets/sountrack.mp3" type="audio/mp3" />
  </audio>
  <Sidebar />
  <div class="container">
    <button @click="playMusic('playAudio')" class="toggler">play</button>
  </div>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  font-family: Iosevka;
}
body {
  min-height: 100%;
  min-width: auto;
  background: url("https://wallpapercave.com/wp/wp6389327.jpg") no-repeat;
  background-size: cover;
}
.container {
  height: 100vh;
  width: 30vw;
  background: #1d20213d;
  backdrop-filter: blur(20px);
  color: #fbf1c7;
}
.toggler {
  z-index: 10000;
  border: 0;
  background: none;
  color: #fbf1c7;
}
</style>
