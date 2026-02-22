<template>
  <div class="ElementContainer">
    <button class="round-btn">
        <div class="icon-wrapper">
            <img src="../assets/mio.png" alt="icon" class="custom-icon" />
        </div>
    </button>
    <p>Mio</p>
  </div>
</template>

<style scoped>
.ElementContainer{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.round-btn {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  
  border: none;
  outline: none;
  cursor: pointer;
  
  background-color: #e1f5fe;
  
  /* Centrage de l'icône */
  display: flex;
  align-items: center;
  justify-content: center;
  
  /* Ombre (Shadow) extraite de ton code */
  box-shadow: 0 2px 2px 0 rgba(0,0,0,.14),
              0 3px 1px -2px rgba(0,0,0,.12),
              0 1px 5px 0 rgba(0,0,0,.2);
              
  /* Animation */
  transition: box-shadow 0.2s ease-out, background-color 0.2s ease-out;
}

.round-btn:hover {
  background-color: #6EC8FF; /* Un bleu un peu plus foncé au survol */
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.icon-wrapper {
  width: 100%;  /* Taille de l'icône interne */
  height: 100%;
  display: flex;
}

.custom-icon {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

p{
  margin: 6px;
  font-family: Roboto, Arial, sans-serif;
  font-size: 15px;
  color: #333;
  -webkit-text-size-adjust: 100%;
}
</style>