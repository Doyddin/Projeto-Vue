<script setup>
import { ref } from 'vue'
</script>
<template>
  <!-- <nav class="navbar text-light bg-dark border-bottom border-body" data-bs-theme="dark">
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <router-link class="navbar-brand" to="/">Pokedex</router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" aria-current="page" to="/">Início</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/about">Sobre</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </nav> -->

  <div class="main">
    <router-view></router-view>
  </div>


  <footer class="bg-dark text-light">
    <div>
      Unimar | ADS | {{ new Date().getFullYear() }}
    </div>
  </footer>

  <link rel="stylesheet" href="\assets\css\main.css">
</template>
