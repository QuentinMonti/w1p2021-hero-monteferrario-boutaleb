<template>
  <div class="big-header">
    <h1>{{ title }}</h1>
    <br>
    <router-link class="button" to="/Character">Choix des personages</router-link>
    <br>
    <button class="button" @click="handleClick">Click me up</button>
  </div>
</template>

<script>
import countService from "../services/countService";

export default {
  data() {
    return {
      title: "SpaceOdyssey"
    };
  },
  methods: {
    handleClick() {
      countService.increment();
    }
  }
};
</script>
