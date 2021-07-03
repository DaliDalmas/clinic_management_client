<template>
  <div id="app">
    <div class="side-pane">
      <img src="../public/logo.png" alt="dalicodeslogo" class="logo" />
    </div>
    <img
      src="../public/stethoscope.png"
      alt="stethoscope"
      class="stethoscope"
    />
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
.stethoscope {
  display: absolute;
  height: 90vh;
  min-width: 60vw;
  margin: 2rem;
}
.side-pane {
  background: rgba(255, 255, 255, 0);
  position: relative;
  top: 0;
  bottom: 0;
  left: 0;
  width: 10vw;
  min-height: 80vh;
  border-style: solid;
  border-right-width: thin;
  border-right-color: #7c89c1;
  display: block;
  padding-top: 5rem;
  padding-right: 5rem;
}
.logo {
  transform: rotate(270deg);
  height: 12rem;
  position: absolute;
  left: -5vw;
}
.lower-glass {
  position: absolute;
  left: 10vw;
  right: 0;
  bottom: 0;
  height: 43vh;
  background: rgba(0, 0, 0, 0.103);
  backdrop-filter: blur(2rem);
}

.head-clinic {
  color: #f8f5f5;
  position: absolute;
  left: 50%;
  top: 1%;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  font-size: 3rem;
  font-weight: bold;
  transform: translateX(-50%);
}
.description-clinic {
  padding: 0;
  margin: 0;
  color: #f8f5f5;
  position: absolute;
  font-family: "Poppins", "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  font-size: 1.5rem;
  font-weight: bold;
  top: 15%;
  left: 65%;
  width: 14vw;
  text-align: left;
  border-color: teal;
  border-width: 1px;
}
.signup-container {
  color: white;
  position: absolute;
  top: 27%;
  left: 65%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  z-index: 2;
}
.signup-container input {
  margin-top: 1.5rem;
  width: 27vw;
  height: 5vh;
  border-radius: 10px;
  border: none;
  padding: 1rem;
  cursor: text;
  font-family: "Poppin", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2rem;
}
.input-coat {
  position: relative;
}
.lable {
  position: absolute;
  height: 5vh;
  color: black;
  bottom: 0;
  left: 0;
}
</style>
