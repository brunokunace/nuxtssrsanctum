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
  methods: {
      async loadUsers () {
        this.users = await this.$axios.$get('/users')
      }
  },
  async mounted() {
    await this.loadUsers()
  }
}
</script>

<style scoped>

</style>
