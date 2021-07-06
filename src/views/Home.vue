<template>
  <div class="home">
    <div class="head-clinic">CLINIC MANAGEMENT SYSTEM</div>
    <div class="description-clinic">MANAGING AND KEEPING YOUR CLINIC DATA</div>
    <input
      type="button"
      :value="topButtonValue"
      class="btn login"
      @click="loginView"
    />
    <SignupContainer v-if="signup" :signup="signUpFn" />
    <LoginContainer v-if="!signup" />
    <LowerGlass />
  </div>
</template>

<script>
import LowerGlass from "../components/lowerGlass.vue";
import SignupContainer from "../components/signup.vue";
import LoginContainer from "../components/login.vue";
export default {
  name: "Home",
  components: { LowerGlass, SignupContainer, LoginContainer },
  data() {
    return {
      signup: true,
      topButtonValue: "LOGIN",
    };
  },
  methods: {
    signUpFn() {
      this.signup = false;
    },
    loginView() {
      this.signup = !this.signup;
      if (this.signup) {
        this.topButtonValue = "LOGIN";
      } else {
        this.topButtonValue = "SIGN UP";
      }
    },
  },
};
</script>
