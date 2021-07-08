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
.input-class {
  margin-top: 1.5rem;
  width: 27vw;
  height: 5vh;
  border-radius: 10px;
  border: none;
  outline: none;
  padding: 1rem;
  cursor: text;
  font-family: "Poppin", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2rem;
}

.input-coat {
  position: relative;
}
.lable {
  font-family: "Poppin", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1rem;
  position: absolute;
  height: 5vh;
  color: rgb(36, 35, 35);
  bottom: 0;
  left: 0em;
  padding: 1rem;
}

.btn {
  cursor: pointer;
  background: rgba(0, 217, 255, 0.534);
  margin-top: 1.5rem;
  width: 27vw;
  height: 5vh;
  border-radius: 10px;
  border: none;
  color: white;
  font-weight: bold;
  font-size: 1.5rem;
  transition: ease 0.5s;
}
.btn:active {
  transform: scale(0.9);
}
.login {
  width: 10vw;
  position: absolute;
  right: 8vw;
  height: 4vh;
  background: rgba(0, 217, 255, 0.205);
  color: rgba(255, 255, 255, 0.555);
  transition: ease 0.5s;
}
.login:hover {
  background: rgba(0, 217, 255, 0.534);
  color: white;
  transform: scale(1.05);
}

.lable {
  transition: ease 0.5s;
  width: 100%;
  text-align: left;
  pointer-events: none;
}
.dates {
  text-align: center;
}
.input-class:focus + .lable,
.input-class:valid + .lable {
  transform: translateY(-75%);
  color: white;
}
.patients {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
.middle-glass {
  position: absolute;
  min-height: 70vh;
  min-width: 80vw;
  background: rgba(0, 0, 0, 0.144);
  backdrop-filter: blur(2rem);
  transform: translateX(-25%);
}
.patients-container {
  position: absolute;
  height: 69vh;
  min-width: 80vw;
  transform: translateX(-25%);
  z-index: 3;
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
  flex: 1 1 auto;
  overflow-y: scroll;
}
.patient-card {
  height: 200px;
  width: 390px;
  background: rgba(255, 255, 255, 0.5);
  display: flex;
  margin: 1rem;
  border-radius: 10px;
  color: black;
  cursor: pointer;
}
.profile-image {
  border-radius: 10px;
  flex: 1;
}
.profile-content {
  flex: 1;
  border-radius: 10px;
}
.profile-content-top {
  border-bottom: black;
  border-style: solid;
  border-width: 0 0 1px 0;
}
.profile-content-bottom {
  display: flex;
  justify-content: space-around;
  padding: 1rem;
  flex-direction: column;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.fnlname {
  font-family: "Poppin", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin-top: 1rem;
  font-size: 1.2rem;
  font-weight: bold;
}
.age {
  font-family: "Poppin", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin-bottom: 1rem;
  margin-top: 1rem;
  font-size: 1rem;
  font-weight: bold;
}
.patient-ribbon {
  position: absolute;
  top: 12%;
  left: 0;
  color: white;
  z-index: 4;
  background: red;
  width: 80vw;
  transform: translateX(-75%);
  display: flex;
  justify-content: space-between;
  font-family: "Poppins", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bold;
  font-size: 1.1rem;
}
</style>
