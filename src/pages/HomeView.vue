<script setup>
    import MioButton from '@/components/MioButton.vue';
    import LeaButton from '@/components/LeaButton.vue';
    import ServiceSection from '@/components/ServiceSection.vue';
    import NewsSection from '@/components/NewsSection.vue';
    import EventSection from '@/components/EventSection.vue';

    //https://arr.cornhub.website/
</script>

<template>
    <div class="container">
        <img class="banner" src="../assets/banner.png" alt="Bannière obnibox">

        <div class="body-layout">
            <div class="sidePannel">
                <div class="circularButtonArea">
                    <LeaButton/>
                    <MioButton />
                </div>

                <ServiceSection/>
            </div>

            <div class="mainContent">
                <NewsSection/>
                <EventSection class="event-section"/>
            </div> 
        </div>
    </div>
</template>

<style scoped>
.container{
    background-color: #fafafa;
    display: flex;
    flex-direction: column;
}
.body-layout {
    display: flex;
    flex: 1;
    width: 100%;
}
.mainContent{
    display: flex;
    flex: 1;
    align-items: flex-start;
    flex-direction: column;
}

.event-section{
    margin-top: 50px;
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
    background-color: #ffffff;
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