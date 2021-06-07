<template>
    <img alt="EOFIS logo" src="../assets/logo.png">
<HomeBody/>
</template>

<script>
// @ is an alias to /src
import HomeBody from '@/components/HomeBody.vue'

export default {
  name: 'Home',
  components: {
    HomeBody
  }
}
</script>

<style scoped>
img {
width: 30%;
}

</style>
