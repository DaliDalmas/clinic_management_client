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
import axios from "axios";
export default {
  name: "Home",
  components: { LowerGlass, SignupContainer, LoginContainer },
  data() {
    return {
      signup: true,
      topButtonValue: "LOGIN",
      sigup_url: "http://127.0.0.1:8000/user/management/register",
    };
  },
  methods: {
    signUpFn(fname, lname, email, date, sex, position, pass1, pass2) {
      if (pass1 != pass2) {
        console.log("Psswords dont match");
      } else {
        axios
          .post(this.sigup_url, {
            email: email,
            password: pass1,
            first_name: fname,
            last_name: lname,
            position: position,
            gender: sex,
            date_of_birth: date,
          })
          .then((res) => {
            console.log(res);
          });
        this.signup = false;
      }
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
