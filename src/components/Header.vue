<script setup lang="ts">
defineProps<{
  title: string
}>();
</script>

<template>
  <header class="top-bar">
    <div class="left-section">
      <router-link to="/" class="back-btn">
        <img src="../assets//logo.png" alt="Logo Omnivox" class="logo" />
        <h1 class="title">Obnibox</h1>
      </router-link>
    </div>
    <div class="right-section">
        <p class="student-name">Étudiant</p>
        <p class="school-name">Cégep de Sainte-Foy</p>
    </div>
  </header>
</template>

<style scoped>
.top-bar {
  height: 60px;
  background: #ffffff;
  border-bottom: 1px solid #ddd;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0;
  margin: 0
}

.left-section {
  display: flex;
  align-items: center;
  height: 100%;
}
.right-section{
    display: flex;
    flex-direction: column;
    align-items: end;
    justify-content: center;
    margin-right: 30px;
}

.back-btn{
    display: flex;
    flex-direction: row;
    align-items: center;
    text-decoration: none;
    height: 100%;
    padding: 0 20px;
}
.back-btn:hover {
  background: #D9D9D9;
}

.logo{
    height: 50px;
    width: auto;
    margin-right: 10px;
}
.title{
    color: #0169b0;
}

.student-name{
    /* Typographie */
    font-family: 'Roboto', Arial, Helvetica, sans-serif;
    font-size: 14.5px;
    line-height: 17.5px;
    letter-spacing: 0.7px;
    color: #777676;
    text-align: right;

    /* Espacement */
    margin: 0;
    padding: 0;

    /* Gestion du texte long (tronquage) */
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
.school-name{
    /* Typographie */
    font-family: 'Roboto', Arial, Helvetica, sans-serif;
    font-size: 14.5px;
    line-height: 17.5px;
    font-weight: 700; /* Texte en gras */
    letter-spacing: 0.7px;
    color: #656565; /* Gris plus foncé que l'école */
    text-align: right;

    /* Espacement et Structure */
    margin: 0;
    padding: 0;
    text-decoration: none;

    /* Tronquage si le nom est trop long */
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
</style>