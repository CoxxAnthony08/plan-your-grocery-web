<template>
  <v-container>
    <h1 class="mb-3 display-1">GROCERY LIST (10)</h1>
    <v-row>
      <v-col @click.prevent="">
        <v-hover v-slot="{ hover }" class="cursor-pointer">
          <v-card :elevation="hover ? 12 : 2" :class="{ 'on-hover': hover }" max-width="200" max-height="300">
            <v-img
              :max-height="300"
              :max-width="200"
              :src="hover ? '' : '/img/list.jpg'"
            >
              <v-card-title class="title black--text" v-if="hover">
                <v-row class="fill-height flex-column" justify="space-between">
                  <p class="mt-4 subheading text-left">
                    Grocery list title
                  </p>
                  <p class="mt-4">
                    Created on 
                  </p>
                </v-row>
              </v-card-title>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      groceryLists: []
    }
  }
}
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.9;
 }
</style>