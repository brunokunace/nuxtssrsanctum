<template>
  <div>
    <p>Users</p>
    <pre>{{ users }}</pre>
  </div>
</template>

<script>
export default {
    name: "Users",
    data() {
      return {
        users: []
      }
    },
    async asyncData({ $axios }) {
      const users = await $axios.$get('/users')
      return { users }
    }
}
</script>

<style scoped>

</style>
