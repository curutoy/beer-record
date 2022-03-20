<template>
  <v-navigation-drawer
    v-model="isActive"
    absolute
    temporary
  >
    <v-list
      nav
      dense
    >
      <v-list-item-group
        v-model="group"
        active-class="deep-purple--text text--accent-4"
      >
        <v-list-item>
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-title>
            <router-link to="/">Go to Home</router-link>
          </v-list-item-title>
        </v-list-item>

        <v-list-item>
          <v-list-item-icon>
            <v-icon>mdi-account</v-icon>
          </v-list-item-icon>
          <v-list-item-title>
            <router-link to="/user">Go to User</router-link>
          </v-list-item-title>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    group: null,
  }),
  computed: {
    isActive: {
      get(){
        return this.$store.state.sidebar;
      },
      set(val) {
        this.$store.commit("SIDEBAR", val)
      }
    }
  }
}
</script>
