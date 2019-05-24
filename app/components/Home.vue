<template>
  <div class="big-header">
    <br>
    <ul>
      <li>
        <router-link class="button-home" to="/character">EMBARQUER</router-link>
      </li>
    </ul>
  </div>
</template>



<style lang="scss" scoped>
.big-header {
  background-image: url("../assets/image/home.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  flex-direction: column;
  height: 100vh;
}
</style>

