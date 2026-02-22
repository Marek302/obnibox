<script setup>
import Header from './components/Header.vue';
</script>

<template>
  <div class="app-layout">
    <div class="main-container">
      <Header title="Portail des services" />
      <router-view />
    </div>
  </div>
</template>

<style>
  .app-layout{
    display: flex;
    height: 100vh;
  }
  .main-container{ 
    flex: 1;
    display: 
    flex; 
    flex-direction: column; 
  }

  html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
  }

  * {
    box-sizing: border-box;
  }
</style>
