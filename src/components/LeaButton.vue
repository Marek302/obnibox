<script setup>
  import { useRouter } from 'vue-router';

  const router = useRouter();

  const goToLea = () => {
    router.push('/lea'); 
    setTimeout(() => {
      window.open('https://www.temu.com/', '_blank');
    }, 100);
  };
</script>

<template>
  <div class="ElementContainer">
    <button class="round-btn" @click="goToLea">
        <div class="icon-wrapper">
            <img src="../assets/lea.png" alt="icon" class="custom-icon" />
        </div>
    </button>
    <p>Léa</p>
  </div>
</template>

<style scoped>
.ElementContainer {
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
  
  background-color: #E8FFEA;
  
  display: flex;
  align-items: center;
  justify-content: center;
  
  /* Ombre ShadowDefault extraite */
  box-shadow: 0 2px 2px 0 rgba(0,0,0,.14),
              0 3px 1px -2px rgba(0,0,0,.12),
              0 1px 5px 0 rgba(0,0,0,.2);
              
  transition: .3s ease-out;
  transition-property: box-shadow, background-color;
}

.round-btn:hover {
  background-color: #7fd81f;
  /* Ombre ShadowActive extraite */
  box-shadow: 0 0 8px -2px rgba(0, 0, 0, 0.1), 
              0 6px 20px -3px rgba(0, 0, 0, 0.2);
}

.icon-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.custom-icon {
  width: auto;
  height: 100%;
}

p{
  margin: 6px;
  font-family: Roboto, Arial, sans-serif;
  font-size: 15px;
  color: #333;
  -webkit-text-size-adjust: 100%;
}
</style>