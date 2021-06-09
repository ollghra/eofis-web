<template>
<nav class="navbar is-transparent is-fixed-top">
  <div class="navbar-brand">
    <router-link class="navbar-item" to="/">
      <img src="android-chrome-192x192.png" alt="EOFIS: a new learning tool">
    </router-link>
    <router-link class="navbar-item" to="/">Home</router-link>
<!--    <router-link class="navbar-item" to="/about">About</router-link>-->
    <router-link class="navbar-item" to="/articles">Sample Articles</router-link>
<!--
    <div class="navbar-burger" data-target="navbar">
      <span></span>
      <span></span>
      <span></span>
    </div>
-->
  </div>

  <div id="navbar" class="navbar-menu">
    <div class="navbar-start">
    </div>

    <div class="navbar-end">
    </div>
  </div>
</nav>
<router-view/>
</template>
