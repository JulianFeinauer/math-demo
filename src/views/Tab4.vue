<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 4 is here</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 3</ion-title>
        </ion-toolbar>
      </ion-header>
      
      <Question x="5" y="4" result="9"/>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
// import ExploreContainer from '@/components/ExploreContainer.vue';
import Question from '@/components/Question.vue';

export default  {
  name: 'Tab4',
  components: { Question, IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
}
</script>
