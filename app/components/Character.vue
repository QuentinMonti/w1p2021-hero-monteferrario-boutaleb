<template>
  <div class="big-header">
    <h1>Previous clicks {{ count }}</h1>
    <br>
    <router-link class="button" to="/">Retourner a la homepage</router-link>
    <br>
    <router-link class="button" to="/game/:1">Mike</router-link>
    <router-link class="button" to="/game/:">Sarah</router-link>
  </div>
</template>

<script>
import countService from "../services/countService";

export default {
  data() {
    return {
      count: countService.value()
    };
  }
};
</script>
