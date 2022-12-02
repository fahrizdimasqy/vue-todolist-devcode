<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-container>
        <h2>To Do List App</h2>
      </v-container>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
