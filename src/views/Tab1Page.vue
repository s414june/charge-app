<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>
      <div id="helloContainer">
        <h1>
          hello world
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :icon="heart"></ion-icon>
          <ion-icon :ios="logoApple" :md="logoAndroid"></ion-icon>
        </h1>
      </div>
      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script>
import { heart,logoAndroid, logoApple } from "ionicons/icons";
import { defineComponent } from "vue";
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue";
import ExploreContainer from "@/components/ExploreContainer.vue";

export default defineComponent({
  name: "Tab1Page",
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
  },
  setup() {
    return { heart,logoAndroid, logoApple };
  },
});
</script>
<style>
#helloContainer {
  display: flex;
  justify-content: center;
}
</style>
