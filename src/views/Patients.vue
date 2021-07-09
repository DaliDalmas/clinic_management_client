<template>
  <div class="patients">
    <input type="button" value="SIGN OUT" class="logout-btn" />

    <div class="patient-ribbon">
      <div>Patients</div>
      <div class="register-patient">
        Register Patient
        <div class="add-patient-button">
          <div class="viertical-line"></div>
          <div class="horizontal-line"></div>
        </div>
      </div>
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
