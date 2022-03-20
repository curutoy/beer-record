<template>
  <v-app-bar elevation="4" app>
    <v-app-bar-nav-icon @click="drawer"></v-app-bar-nav-icon>

    <v-toolbar-title>Page title</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn icon>
      <v-icon>mdi-heart</v-icon>
    </v-btn>
  </v-app-bar >
</template>

<script>

export default {

  data: () => ({
  }),
  methods: {
    drawer() {
      this.$store.commit('SIDEBAR', true)
    }
  }
};
</script>
