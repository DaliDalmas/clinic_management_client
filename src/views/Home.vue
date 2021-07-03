<template>
  <div class="home">
    <div class="head-clinic">CLINIC MANAGEMENT SYSTEM</div>
    <div class="description-clinic">MANAGING AND KEEPING YOUR CLINIC DATA</div>
    <SignupContainer />
    <LowerGlass />
  </div>
</template>

<script>
import LowerGlass from "../components/lowerGlass.vue";
import SignupContainer from "../components/signup.vue";
export default {
  name: "Home",
  components: { LowerGlass, SignupContainer },
};
</script>
