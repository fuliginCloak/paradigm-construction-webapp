<template>
  <v-container>
    <v-layout>
      <v-flex xs12>
        <h1>Services</h1>
        <li>Plumbing</li>
        <li>HVAC</li>
        <li>Electrical</li>
        <li>Remodeling</li>
        <li>General repairs</li>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  //
}
</script>

<style scoped>
h1 {
  display: flex;
  justify-content: center;
  text-decoration: underline;
}
li {
  display: flex;
  justify-content: center;
  list-style-type: circle;
}
</style>
