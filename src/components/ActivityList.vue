<template>
  <v-container>
    <div class="d-flex justify-space-between mt-5">
      <h2>Activity</h2>
      <v-btn rounded color="info" dark large>
        <v-icon dark> mdi-plus </v-icon>
        Tambah
      </v-btn>
    </div>
    <ActivityEmptyStateVue class="mt-15" />
  </v-container>
</template>

<script>
import ActivityEmptyStateVue from "./ActivityEmptyState.vue";
export default {
  name: "ActivityList",
  components: {
    ActivityEmptyStateVue,
  },
};
</script>
