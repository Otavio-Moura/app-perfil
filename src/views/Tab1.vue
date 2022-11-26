<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Meu Perfil</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <img
        id="foto_de_perfil"
        src="https://criticalhits.com.br/wp-content/uploads/2022/11/chrome_3krfIKFgvw-910x512.jpg"
      />

      <h3 id="nome_de_usuario">Mr FlashBlack</h3>

      <p id="bio_de_usuario">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue";

import { ref } from "vue";

export default {
  name: "Perfil",
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
  setup() {
    const user = ref({
      imagem: `https://criticalhits.com.br/wp-content/uploads/2022/11/chrome_3krfIKFgvw-910x512.jpg`,
      nome: `Mr FlashBlack`,
      bio: `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.`,
    });

    return {
      user
    };
  },
};
</script>

<style scoped>
ion-content {
  text-align: center;
}

#foto_de_perfil {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin: 3em auto;
  filter: invert() hue-rotate(90deg) drop-shadow(0px 0px 40px purple);
}

#nome_de_usuario {
  color: darkred;
}

#bio_de_usuario {
  width: 250px;
  margin: 3em auto;
}
</style>