<template>
  <div class="signup-container">
    <div class="input-coat">
      <input
        type="text"
        class="input-class"
        autocomplete="off"
        v-model="fname"
        required
      />
      <div class="lable">
        <span>First Name</span>
      </div>
    </div>
    <div class="input-coat">
      <input
        type="text"
        class="input-class"
        autocomplete="off"
        v-model="lname"
        required
      />
      <div class="lable"><span class="content-name">Last Name</span></div>
    </div>
    <div class="input-coat">
      <input
        type="email"
        class="input-class"
        autocomplete="off"
        v-model="email"
        required
      />
      <div class="lable"><span>Email</span></div>
    </div>
    <div class="input-coat">
      <input
        type="date"
        class="input-class dates"
        autocomplete="off"
        v-model="date"
        required
      />
      <div class="lable"><span>Date of birth</span></div>
    </div>
    <div class="input-coat">
      <input
        type="text"
        class="input-class"
        autocomplete="off"
        v-model="sex"
        required
      />
      <div class="lable"><span>sex</span></div>
    </div>
    <div class="input-coat">
      <input
        type="text"
        class="input-class"
        autocomplete="off"
        v-model="position"
        required
      />
      <div class="lable"><span>Position</span></div>
    </div>
    <div class="input-coat">
      <input
        type="password"
        class="input-class"
        autocomplete="off"
        v-model="pass1"
        required
      />
      <div class="lable"><span>Password</span></div>
    </div>
    <div class="input-coat">
      <input
        type="password"
        class="input-class"
        autocomplete="off"
        v-model="pass2"
        required
      />
      <div class="lable"><span>Confirm password</span></div>
    </div>
    <input
      type="button"
      value="SIGN UP"
      class="btn"
      @click="signup(fname, lname, email, date, sex, position, pass1, pass2)"
    />
  </div>
</template>
<script>
export default {
  props: ["signup"],
  data() {
    return {
      fname: "",
      lname: "",
      email: "",
      date: "",
      sex: "",
      position: "",
      pass1: "",
      pass2: "",
    };
  },
};
</script>
