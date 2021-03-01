<template>
  <div>
      <v-text-field
            label="User Name"
          ></v-text-field>
           <v-text-field
           label="Password"
            type="password"
          ></v-text-field>
          <v-btn
          @click="login"
  elevation="2"
>Log in</v-btn>
  </div>
</template>

<script>
export default {
  layout:'login',
    methods: {
        login(){
            this.$router.push('/home')
        }
    }
}
</script>

<style>

</style>