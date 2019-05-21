<template>
  <div class="big-header">
    <h1>{{step.title}}</h1>
    <ul>
      <li v-for="action in step.actions" v-bind:action="action" v-bind:key="action.title">
        <router-link class="button" :to="action.to.toString()">{{ action.title }}</router-link>
      </li>
    </ul>
    <img>
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
