<script setup>
</script>

<template>
  <div class="event-wrapper">
    <div class="event-header">
      <h2 class="event-title">Évènements</h2>
      <a href="#" class="view-all">
        Voir tout
        <span class="material-icons">view_module</span>
      </a>
    </div>

    <div class="event-content-placeholder">
      <p class="no-events">Aucun évènement à venir pour le moment.</p>
    </div>
  </div>
</template>

<style scoped>
.event-wrapper {
  /* Tes variables copiées */
  --lt-color-gray-100: #f8f9fc;
  --lt-color-gray-200: #f1f3f9;
  --lt-color-gray-300: #dee3ed;
  --lt-color-gray-400: #c2c9d6;
  --lt-color-gray-500: #8f96a3;
  --lt-color-gray-600: #5e636e;
  --lt-color-gray-700: #2f3237;
  --lt-color-gray-800: #1d1e20;
  --lt-color-gray-900: #111213;

  font-family: Roboto, Arial;
  text-align: left;
  padding: 0;
  margin: 0;
  margin-left: 30px;
  max-width: 1000px;
  margin-bottom: 44px; 
  width: 90%;
}

.event-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  border-bottom: 2px solid #C7C7C7;
  padding-bottom: 2px;
  margin-bottom: 20px;
}

.event-title {
  font-size: 24px;
  font-weight: 500;
  color: #cd4d02; /* Orange Omnivox */
  margin: 0;
  line-height: 1;
}

.view-all {
  color: #0169b0;
  text-decoration: none;
  font-size: 14px;
  display: flex;
  align-items: center;
}

.material-icons {
  font-family: 'Material Icons';
  font-weight: normal;
  font-style: normal;
  font-size: 26px; /* Ta valeur copiée */
  line-height: 1;
  letter-spacing: normal;
  text-transform: none;
  display: inline-block;
  white-space: nowrap;
  word-wrap: normal;
  direction: ltr;
  -webkit-font-smoothing: antialiased;
  text-rendering: auto;
  margin-left: 6px;
  vertical-align: middle;
  color: #0169b0;
}

.no-events {
  color: var(--lt-color-gray-600);
  font-size: 15px;
  margin-top: 10px;
}
</style>