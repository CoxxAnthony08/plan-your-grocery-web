<template>
  <v-container>
    <h1 class="mb-3 display-1">Submit a Product</h1>
    <v-row>
      <v-col cols="3">
        <v-text-field label="Product Name">
        </v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3">
        <v-autocomplete
          label="Product Type"
        ></v-autocomplete>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3">
        <v-autocomplete
          label="Manufacturer"
        ></v-autocomplete>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-btn color="primary">Submit Product</v-btn>
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