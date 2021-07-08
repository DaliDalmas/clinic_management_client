<template>
  <div class="patients">
    <div class="patient-ribbon">
      <div>Patients</div>
      <div>Register Patient</div>
    </div>
    <div class="patients-container">
      <patientCard
        v-for="(item, index) in patientsData"
        :key="index"
        :items="item"
      />
    </div>
    <middleGlass />
  </div>
</template>
<script>
import middleGlass from "../components/middleGlass.vue";
import patientCard from "../components/patientCard.vue";
import patientData from "../assets/patients";
export default {
  components: { middleGlass, patientCard },
  data() {
    return {
      topButtonValue: "SIGN OUT",
      patientsData: patientData.patientData,
    };
  },
};
</script>

