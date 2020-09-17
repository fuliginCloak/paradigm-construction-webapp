<template>
  <v-container>
    <v-layout> </v-layout>
    <v-img class="image-bg-home" src="@/assets/Static/Images/temp1.jpg"></v-img>

    <vue-typed-js
      class="hidden-md-and-down"
      :strings="['Time Quality Focus Drive.']"
      :typeSpeed="80"
      :showCursor="false"
      :fadeOut="true"
      :fadeIn="true"
      :fadeOutDelay="500"
      :startDelay="1000"
    >
      <p class="typing"></p>
    </vue-typed-js>
  </v-container>
</template>

<style scoped>
* {
  padding: 0;
  margin: 0;
}

.image-bg-home {
  height: 360px;
  margin-top: 10%;
  opacity: 40%;
  width: 100%; /* fall back */
  width: 100vw;
  position: absolute;
  background-repeat: no-repeat;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

p {
  z-index: 100;
  position: absolute;
  font-size: 26px;
  font-weight: bold;
  left: 150px;
  top: 360px;
}
</style>
