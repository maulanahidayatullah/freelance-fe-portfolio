<template>
  <v-app-bar app color="black" class="px-12">
    <v-img class="px-2 pt-6" src="../assets/logo.png" max-height="100" max-width="100"></v-img>
    <!-- <v-toolbar-title class="ml-2">
      LIKE PROJECT
    </v-toolbar-title> -->
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-red">Home</v-btn>
    <v-btn text @click="scroll('about')">Portfolio</v-btn>
  </v-app-bar>
</template>

<script>

export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style></style>