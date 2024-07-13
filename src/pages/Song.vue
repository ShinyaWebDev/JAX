<template>
  <v-container class="song" fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" class="text-center">
        <h2 class="headline">Manage Your Songs</h2>
        <v-btn class="my-4" color="primary" @click="showDialog = true"
          >Upload Song</v-btn
        >
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12" md="6" class="d-flex justify-center">
        <v-responsive aspect-ratio="16/9" @click.stop>
          <div class="overlay" v-if="showOverlay"></div>
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/yaGD5BCPrwQ?si=NEurtm_Glyr0ku-N"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </v-responsive>
      </v-col>
      <v-col cols="12" md="6" class="d-flex justify-center">
        <v-responsive aspect-ratio="16/9" @click.stop>
          <div class="overlay" v-if="showOverlay"></div>
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/Eeprlu37nZc?si=GX_D9F6lO1idqqAk"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </v-responsive>
      </v-col>
    </v-row>
    <v-dialog v-model="showDialog" max-width="290">
      <v-card>
        <v-card-text class="mt-2">ごめんよ、ちょっと待ってね😘</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" @click="showDialog = false">閉じる</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script lang="ts" setup>
const showDialog = ref(false);
const showOverlay = ref(true);

// Hide overlay after iframe loads
const hideOverlay = () => {
  showOverlay.value = false;
};
</script>

<style scoped>
.song {
  text-align: center;
  margin-top: 10vh;
}
.v-responsive {
  margin: 20px 0;
  position: relative;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.01); /* Transparent overlay */
  z-index: 1;
}
</style>
