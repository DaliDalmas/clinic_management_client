<template>
  <div class="signup-container">
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Email</span></div>
    </div>

    <div class="input-coat">
      <input type="password" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Password</span></div>
    </div>
    <input type="button" value="LOGIN" class="btn" @click="loginFn" />
  </div>
</template>
<script>
export default {
  methods: {
    loginFn() {
      this.$router.push({ name: "Patients" });
    },
  },
};
</script>
