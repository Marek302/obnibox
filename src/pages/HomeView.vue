<script setup>
    import MioButton from '@/components/MioButton.vue';
    import LeaButton from '@/components/LeaButton.vue';
    import ServiceSection from '@/components/ServiceSection.vue';
</script>

<template>
    <div class="container">
        <img class="banner" src="../assets/banner.png" alt="Bannière obnibox">

        <div class="sidePannel">
            <div class="circularButtonArea">
                <LeaButton/>
                <MioButton />
            </div>

            <ServiceSection/>
        </div>
    </div>
</template>

<style scoped>
.container{
    background-color: #E8E8E8;
    height: 100vh;
}
.banner{
  width: 100%;     
  display: block;  
  height: auto;      
  max-height: 180px;
  object-fit: cover;
}

.sidePannel{
    display: flex;
    flex-direction: column;
    background-color: #fafafa;
    width: 20%;
    height: 100%;
}
.circularButtonArea{
    display: flex;
    width: 100%;
    margin-left: 7%;
    margin-top: 6%;
    gap: 20px
}
</style>