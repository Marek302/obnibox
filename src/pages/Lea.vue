<script setup>
    import { ref, onMounted } from 'vue';
    import MioButton from '@/components/MioButton.vue';
    import LeaButton from '@/components/LeaButton.vue';
</script>

<template>
    <div class="container">
        <img class="banner" src="../assets/leaBanner.png" alt="Bannière de léa">

        <div class="mainContent">
            <div class="leftArea">
                <LeaButton/>
                <MioButton />
            </div>
        </div>
    </div>
</template>

<style scoped>
.container{
    background-color: #fafafa;
    display: flex;
    flex-direction: column;
    height: 100%;
}

.banner{
  width: 100%;     
  display: block;  
  height: auto;      
  max-height: 180px;
  object-fit: cover;
}
.leftArea{
    display: flex;
    margin: 30px;
    gap: 20px
}
</style>