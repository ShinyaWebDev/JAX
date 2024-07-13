<template>
  <v-container class="video">
    <v-row justify="center" align="center">
      <v-col class="text-center">
        <h2 class="headline">Record Your Videos</h2>
        <v-btn color="primary" @click="recordVideo">Record Video</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
const recordVideo = () => {
  // Add your video recording logic here
};
</script>

<style scoped>
.video {
  text-align: center;
  margin-top: 20vh;
}
</style>
