<template>
  <v-container>
    <h1 class="mb-3 display-1">PROFILE</h1>
    <v-row>
      <v-col cols="2" class="d-flex flex-column">
        <span>First Name</span>
        <span>John</span>
      </v-col>
      <v-col cols="2" class="d-flex flex-column">
        <span>Last Name</span>
        <span>Doe</span>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="d-flex flex-column">
        <span>Birthday</span>
        <span>January 1, 1970</span>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="pb-0">
        <span class="">Grocery List Created</span>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="py-0">
        <a @click.prevent="$router.push('/grocery-list')" class="text-decoration-none">10</a>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="d-flex flex-column">
        <span>Date Joined</span>
        <span>January 1, 1970</span>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>

</style>