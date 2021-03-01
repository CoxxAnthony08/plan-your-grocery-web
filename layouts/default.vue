<template>
  <v-app>
    <v-app-bar
      fixed
      app
      color="elevation-0"
    >
      <v-toolbar-title @click="goto('/home')">Plan-your-Grocery</v-toolbar-title>
      <v-spacer />
      <v-tooltip
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            @click.prevent="goto('/grocery-list')"
          >
            <v-icon>
              mdi-clipboard-list
            </v-icon>
          </v-btn>
        </template>
        <span>Grocery List</span>
      </v-tooltip>
      <v-tooltip
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            @click.prevent="goto('/profile')"
          >
            <v-icon>
              mdi-account
            </v-icon>
          </v-btn>
        </template>
        <span>Profile</span>
      </v-tooltip>
      <v-tooltip
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            @click.prevent="logout()"
          >
            <v-icon>
              mdi-logout
            </v-icon>
          </v-btn>
        </template>
        <span>Logout</span>
      </v-tooltip>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; All rights reserved {{ new Date().getFullYear() }}.</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      fixed: false
    }
  },
  methods: {
    goto (route) {
      this.$router.push(route)
    },
    logout(){
      this.$router.push('/login')
    }
  }
}
</script>
