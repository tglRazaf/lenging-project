<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">
          <img src="../assets/logo.png" width="50" height="50">
        </router-link>
      </div>
      <div class="navbar-start">
        <div class="navbar-item">
          Space travel
        </div>
      </div>
      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-end">
          <router-link to="/" class="navbar-item">
            Home
          </router-link>
          <router-link to="/about" class="navbar-item">
            About
          </router-link>
          <router-link to="/about" class="navbar-item">
            Contact
          </router-link>
          <router-link to="/about" class="navbar-item">
            Support 
          </router-link>
        </div>
      </div>
    </nav>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class NavBar extends Vue {}
</script>

<style lang="scss" scoped>
  .navbar{
    background-color: transparent !important;

    .navbar-item{
      color: white;
    }

    a.navbar-item:hover{
      border-bottom: 1px solid rgb(45, 28, 61);
      background-color: rgba(57, 39, 70, 0.199);
    }
  }
</style>