<template>
  <div class="patients">
    <middleGlass />
  </div>
</template>
<script>
import middleGlass from "../components/middleGlass.vue";
export default {
  components: { middleGlass },
  data() {
    return {
      topButtonValue: "SIGN OUT",
    };
  },
};
</script>
