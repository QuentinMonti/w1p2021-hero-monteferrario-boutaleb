<template>
  <div class="big-header">
    <br>
    <ul>
      <li>
        <router-link class="button-character" to="/game/16">Sarah</router-link>
      </li>
      <li>
        <router-link class="button-character" to="/game/1">Mike</router-link>
      </li>
    </ul>
  </div>
</template>


<style lang="scss" scoped>
.big-header {
  background-image: url("../assets/image/characters.png");
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
ul {
  display: flex;
  justify-content: space-between;
  width: 970px;
  margin-left: -11px;
  margin-top: 450px;
  li {
    list-style: none;

    .button-character {
      background: linear-gradient(90deg, #000000 0%, #ac4be8 99.85%);
      box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.24),
        0px 0px 2px rgba(0, 0, 0, 0.12);
      border-radius: 10px;
      text-decoration: none;
      background-position: center;
      background-repeat: no-repeat;
      justify-content: space-between;
      flex-direction: row;
      color: white;
      padding: 40px;
      font-size: 24px;
      &:hover {
        color: rgb(233, 236, 16);
      }
    }
  }
}
</style>
