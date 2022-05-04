<template>
  <ion-page class="master">
    <ion-header class="header ion-no-border">
      <ion-grid>
        <ion-row class="ion-align-items-center">
          <ion-col size="2">
            <img src="assets/icon/manflixfundo.png" alt="Manflix">
          </ion-col>

          <ion-col size="10">
            <ion-row>
              <ion-col size="4"><span class="menuHeader">Séries</span></ion-col>
              <ion-col size="4"><span class="menuHeader">Filmes</span></ion-col>
              <ion-col size="4"><span class="menuHeader">Trailers</span></ion-col>
            </ion-row>
          </ion-col>

        </ion-row>
      </ion-grid>
    </ion-header>

    <div class="poster"></div>
    <ion-grid class="buttons">
      <ion-row>
        <ion-col size="4">
          <ion-button color="dark" fill="clear">
            <div>
              <ion-icon class="lblContrast lblIcon" :icon="addOutline"></ion-icon>
              <ion-label class="lblContrast">Minha Lista</ion-label>
            </div>
          </ion-button>
        </ion-col>
        <ion-col size="4">
          <ion-button color="light">
            <div class="btnWatch">
              <ion-icon class="lblIcon" :icon="playOutline"></ion-icon>
              <ion-label class="lblDark">Assistir</ion-label>
            </div>
          </ion-button>
        </ion-col>
        <ion-col size="4">
          <ion-button color="dark" fill="clear">
            <div>
              <ion-icon class="lblContrast lblIcon" :icon="alertCircleOutline"></ion-icon>
              <ion-label class="lblContrast">Saiba Mais</ion-label>
            </div>
          </ion-button>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-page>
</template>

<script>
import { IonHeader, IonPage, IonCol, IonGrid, IonRow } from '@ionic/vue';
import { defineComponent } from 'vue';
import { addOutline, alertCircleOutline, playOutline } from 'ionicons/icons';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonHeader,
    IonPage,
    IonCol,
    IonGrid,
    IonRow
  },
  setup(){
    return {
      addOutline,
      alertCircleOutline,
      playOutline
    }
  }
});
</script>

<style scoped lang="scss">
.master{
  background-color: var(--ion-color-primary);
}
ion-header,
ion-grid,
ion-row,
ion-col{
  color: var(--ion-color-primary-contrast)
}

.header{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1;

  img{
    width: 40px;
  }
}

.menuHeader{
  font-weight: bold;
}

.poster{

  position: relative;
  width: 100%;
  height: 71vh;
  background-image: url("https://poltronanerd.com.br/wp-content/uploads/2018/10/poltrona-daredevil-poster-season3-692x1024.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  -webkit-mask-image: linear-gradient(to top, transparent 0%, black 11%);
}

.buttons{
  margin-top: -40px;
  ion-button div{
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

</style>
