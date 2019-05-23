<template>
  <div class="big-header">
    <h1>{{message}}</h1>
    <br>
    <div class="imageMec"></div>
    <ul>
      <li>
        <router-link class="button" to="/game/1">Mike</router-link>
      </li>
      <li>
        <router-link class="button" to="/game/16">Sarah</router-link>
      </li>
    </ul>
  </div>
</template>


<script>
import data from "../data.json";
export default {
  data() {
    return {
      message:
        "Pour avancer dans votre aventure, il vous faudra faire des choix qui seront parfois décisifs pour votre survie. Commençons simplement, quel est votre nom ?"
    };
  }
};
</script>

