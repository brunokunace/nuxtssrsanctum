<template>
  <a href="#" @click.prevent="login">Login</a>

</template>

<script>
  export default {
    name: "login",
    auth: false,
    methods: {
      async login () {
        await this.$auth.loginWith('laravelSanctum', {
          data: {
            email: 'bruno@bruno.com.br',
            password: '123123'
          }
        })
        this.$router.push('/users')
      }
    }
  }
</script>

<style scoped>

</style>
