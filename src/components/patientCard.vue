<template>
  <div class="patient-card">
    <img
      :src="items.image"
      :alt="items.first_name + items.last_name"
      class="profile-image"
    />
    <div class="profile-content">
      <div class="profile-content-top">
        <div class="fnlname">{{ items.first_name }} {{ items.last_name }}</div>
        <div class="age">{{ items.age }}</div>
      </div>
      <div class="profile-content-bottom">
        <div>{{ items.visits }}</div>
        <div>visits</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["items"],
};
</script>
