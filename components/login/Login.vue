<template>
  <v-container>
    <v-row no-gutters>
      <v-spacer></v-spacer>
      <v-col cols="2">
        <v-card class="px-7 pt-7 pb-2">
          <div class="text-center mb-3">
            <h1 class="title mb-2">Welcome</h1>
            <h2 class="caption mb-2">Log in or Signup to continue</h2>
          </div>
          <v-text-field
            label="Username or Email Address"
          ></v-text-field>
          <v-text-field
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            :type="showPassword ? 'text' : 'password'"
            @click:append="showPassword = !showPassword"
            label="Password"
          ></v-text-field>
          <a href="#" class="text-decoration-none caption">Forgot password?</a>
          <v-btn
            class="my-6"
            color="primary"
            @click="login"
            block
            elevation="2">Continue
          </v-btn>
          <v-divider></v-divider>
          <span class="caption pt-6">Dont have account? <a class="text-decoration-none" @click="$router.push('/signup')">Sign up</a></span>
        </v-card>
      </v-col>
      <v-spacer></v-spacer>
    </v-row>
  </v-container>
</template>

<script>
export default {
  layout:'login',
  data() {
    return {
      showPassword: false
    }
  },
  methods: {
    login(){
      this.$router.push('/home')
    }
  }
}
</script>

<style>

</style>