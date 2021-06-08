<template>
<nav class="navbar is-transparent is-fixed-top">
  <div class="navbar-brand">
    <router-link class="navbar-item" to="/">
      <img src="android-chrome-192x192.png" alt="EOFIS: a new learning tool">
    </router-link>
    <router-link class="navbar-item" to="/">Home</router-link>
    <router-link class="navbar-item" to="/about">About</router-link>
    <router-link class="navbar-item" to="/articles">Articles</router-link>
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
<!--
<section class="hero is-fullheight">
  <div class="hero-head">
    <nav class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item">
            <img src="favicon.ico" alt="Logo"/>
            <span> EOFIS</span>
          </a>
          <span class="navbar-burger" data-target="navbarMenuHeroB">
            <span></span>
            <span></span>
            <span></span>
          </span>
        </div>
        <div id="navbarMenuHeroB" class="navbar-menu">
          <div class="navbar-end">
            <router-link class="navbar-item" to="/">Home</router-link>
            <router-link class="navbar-item" to="/about">About</router-link>
            <router-link class="navbar-item" to="/articles">Articles</router-link>
          </div>
        </div>
      </div>
    </nav>
  </div>

    <router-view/>
</section>
-->
      <!-- <p class="title">         Title      </p>      <p class="subtitle">        Subtitle      </p> -->
<!--
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/articles">Articles</router-link>
  </div>
  <router-view/>
-->
</template>
