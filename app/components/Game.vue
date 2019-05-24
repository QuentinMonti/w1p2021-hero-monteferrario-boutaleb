<template>
  <div class="big-header" v-bind:style="{ backgroundImage: 'url(' + step.background + ')' }">
  <div class="audio-mute" onclick="document.getElementById('music').pause()"><img src="../assets/image/Audio-mute.png" /></div>
  <div class="audio-on" onclick="document.getElementById('music').play()"><img src="../assets/image/audio-on.png" /></div>
    <h1 v-if="$route.params.id">{{step.title}}</h1>
    <audio id="music" src="../assets/audio/interstellar.mp3" autoplay loop></audio>
    <ul>
      <li v-for="action in step.actions" v-bind:action="action" v-bind:key="action.title">
        <router-link class="button" :to="action.to.toString()">{{ action.title }}</router-link>
        <img v-bind:src="action.img">
      </li>
    </ul>
  </div>
</template>


<script>
import game from "../data.json";

export default {
  data: function() {
    return {
      step: this.getStep()
    };
  },

  watch: {
    "$route.params.id"(to, from) {
      this.step = this.getStep();
    }
  },

  methods: {
    getStep() {
      return game.steps.find(step => {
        return step.id === parseInt(this.$route.params.id, 10);
      });
    }
  }
};
</script>
<style lang="scss" scoped>
.big-header {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  overflow: hidden;
}

ul {
  display: flex;
  img {
    height: 500px;
  }
}
</style>


