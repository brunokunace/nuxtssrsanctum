<template>
  <a href="#" @click.prevent="login">Login</a>

</template>

<script>
  export default {
    name: "login",
    auth: false,
    methods: {
      login () {
        this.$auth.loginWith('laravelSanctum', {
          data: {
            email: 'bruno@bruno.com.br',
            password: '123123'
          }
        })
      }
    }
  }
</script>

<style scoped>

</style>
