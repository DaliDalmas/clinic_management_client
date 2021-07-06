<template>
  <div class="signup-container">
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable">
        <span>First Name</span>
      </div>
    </div>
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable"><span class="content-name">Last Name</span></div>
    </div>
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Email</span></div>
    </div>
    <div class="input-coat">
      <input
        type="date"
        class="input-class dates"
        autocomplete="off"
        required
      />
      <div class="lable"><span>Date of birth</span></div>
    </div>
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable"><span>sex</span></div>
    </div>
    <div class="input-coat">
      <input type="text" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Position</span></div>
    </div>
    <div class="input-coat">
      <input type="password" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Password</span></div>
    </div>
    <div class="input-coat">
      <input type="password" class="input-class" autocomplete="off" required />
      <div class="lable"><span>Confirm password</span></div>
    </div>
    <input type="button" value="SIGN UP" class="btn" @click="signup" />
  </div>
</template>
<script>
export default {
  props: ["signup"],
};
</script>
