<template>
  <v-app>
    <Header></Header>
    <SideBar></SideBar>
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: {
    Header,
    SideBar,
  },

  data: () => ({
  }),
};
</script>
