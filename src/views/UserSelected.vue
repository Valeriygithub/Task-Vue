<template>
  <div class="about-wrapper">
    <div>
      <Sidebar />
    </div>
    <div>
      <!-- <Users /> -->
    </div>
  </div>
</template>

<script>
import Sidebar from "@/components/Sidebar.vue";
// import Users from "@/components/Users.vue";

export default {
  name: "UserSelected",
  components: {
    Sidebar,
    // Users,
  },
};
</script>

<style scoped>
.about-wrapper {
  padding-top: 20px;
  max-width: 1400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 350px 1fr;
}
</style>