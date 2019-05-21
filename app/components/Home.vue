<template>
  <div class="big-header">
    <h1>{{ title }}</h1>
    <br>
    <router-link class="button" to="/Character">Choix des personages</router-link>
  </div>
</template>

<script>
//import countService from "../services/countService";

export default {
  data() {
    return {
      title: "SpaceOdyssey"
    };
  }
  /* methods: {
    handleClick() {
      countService.increment();
    }
  } */
};
</script>
