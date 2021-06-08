<template>
<!--    <img alt="EOFIS logo" src="../assets/logo.png"> -->
<section class="section">
<HomeBody/>
  <h1 class="title">What is EOFIS?</h1>
  <h2 class="subtitle">
Learning & retaining
  </h2>
</section>
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
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
section {
        background-image: url(../assets/logo.png) ;
        background-position: center center;
        background-repeat:  no-repeat;
        background-attachment: fixed;
        background-size:  40%;
}
</style>
