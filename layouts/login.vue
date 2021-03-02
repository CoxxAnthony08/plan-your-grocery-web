<template>
  <v-app>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="true"
      app
    >
      <span>&copy; All rights reserved {{ new Date().getFullYear() }}.</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {

}
</script>

<style>

</style>