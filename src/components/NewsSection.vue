<script setup>
</script>

<template>
  <div id="ovx10_wrap_actualites" class="news-wrapper">
    <div class="news-header">
      <h2 class="news-title">Actualités</h2>
      <a href="#" class="view-all">
        Voir tout
        <span class="material-icons">view_module</span>
      </a>
    </div>

    <div class="news-container">
      <ul class="news-grid">
        
        <li class="news-card-container ads-container">
          <div class="news-card ad-slot">
            <div class="card-header ad-banner">
              <img src="../assets/nachos.jpg" alt="superbe veste" class="ad-image">
            </div>
            <div class="card-content">
              <span class="category-tag">Sponsorisé</span>
              <h3>Le tout nouveau nachos disponible à la cafétéria pour seulement 35$!</h3>
              <div class="card-footer">
                <span class="date">Annonce</span>
              </div>
            </div>
          </div>
        </li>

        <li class="news-card-container advertisement-section">
          <div class="news-card ad-slot">
            <div class="card-header ad-banner">
              <img src="../assets/jeeVest.jpg" alt="superbe veste" class="ad-image">
            </div>
            <div class="card-content">
              <span class="category-tag">Promotion</span>
              <h3>Jee vest: Pour un style à couper le souffle</h3>
              <div class="card-footer">
                <span class="date">Sponsorisé</span>
              </div>
            </div>
          </div>
        </li>

      </ul>
    </div>
  </div>
</template>

<style scoped>
.news-wrapper {
  width: 90%;
  max-width: 1000px;
  margin: 28px 0 0 30px;
  font-family: Roboto, Arial, sans-serif;
}

.news-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  border-bottom: 2px solid #C7C7C7;
  margin-bottom: 20px;
}

.news-title {
  font-size: 24px;
  font-weight: 500;
  color: #cd4d02;
  margin: 0;
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
    font-size: 26px;
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

.news-grid {
  display: flex;
  gap: 20px;
  list-style: none;
  padding: 0;
  margin: 0;
  align-items: stretch;
}

.news-card {
  width: 280px;
  height: 100%;
  background: white;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  overflow: hidden;
  border-bottom: 4px solid #003366;
  cursor: pointer;
  transition: transform 0.2s;
}

.news-card:hover {
  transform: translateY(-5px);
}

.card-header {
  height: 140px;
  background: #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-weight: bold;
}

/* Couleurs spécifiques aux pubs pour les repérer */
.ad-banner { background-color: #ff5252; }
.ad-banner.alternate { background-color: #448aff; }

.card-content {
    padding: 15px;
    flex: 1;         
    display: flex;
    flex-direction: column;
}

.category-tag {
  font-size: 11px;
  text-transform: uppercase;
  color: #666;
}

h3 {
  font-size: 16px;
  margin: 10px 0;
  color: #222;
  line-height: 1.4;
}

.card-footer {
  margin-top: auto;
  font-size: 12px;
  color: #999;
  display: flex;
  align-items: center;
  gap: 5px;
}
.ad-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>