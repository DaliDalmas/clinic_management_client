<template>
  <div id="app">
    <div class="side-pane"></div>
    <img src="../public/stethoscope.png" alt="stethoscope" />
    <router-view />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: linear-gradient(to bottom right, #205c98, #1e5339);
  min-height: 100vh;
  display: flex;
}
img {
  display: absolute;
  height: 100vh;
  min-width: 60vw;
  margin: 2rem;
}
.side-pane {
  background: rgb(255, 255, 255);
  border-right: 2px #7C89C1;

  display: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  width: 15vw;
  min-height: 100vh;
  z-index: 100;
}
</style>
