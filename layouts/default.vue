<template>
  <v-app>
    <v-app-bar
      fixed
      app
      color="elevation-0"
    >
      <v-tooltip
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-toolbar-title v-bind="attrs" v-on="on" @click="goto('/home')" class="cursor-pointer">Plan-your-Grocery</v-toolbar-title>
        </template>
        <span>Home</span>
      </v-tooltip>
      <v-spacer />
      <v-tooltip
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            @click.prevent="goto('/home/submit-a-product')"
          >
            <v-icon>
              mdi-plus-box
            </v-icon>
          </v-btn>
        </template>
        <span>Submit a Product</span>
      </v-tooltip>
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
