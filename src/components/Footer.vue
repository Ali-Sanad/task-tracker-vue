<template>
  <footer>
    <p @click="gg()">Copyright &copy; 2022</p>
    <router-link to="/about" v-show="!aboutPage">About</router-link>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    aboutPage() {
      if (this.$route.path === '/about') {
        return true
      } else {
        return false
      }
    },
  },

}

</script>
<style scoped>
a {
  color: #333;
}

footer {
  margin-top: 30px;
  text-align: center;
}
</style>
