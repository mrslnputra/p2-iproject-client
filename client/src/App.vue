<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  created () {
    if (localStorage.getItem('access_token')) {
      this.$store.commit('SET_IS_LOGGED_IN', true)
    } else {
      this.$store.commit('SET_IS_LOGGED_IN', false)
    }
  }
}
</script>
<style>
body{
  background-color: #A7C4BC;
}
</style>
