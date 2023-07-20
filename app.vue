<template>
  <v-app>
  </v-app>
</template>

<script setup lang="ts">
import { useTheme } from "vuetify";
const theme = useTheme();

if (process.client) {
  let media = window.matchMedia("(prefers-color-scheme: dark)");

    function onThemeChange() {
      theme.global.name.value = media.matches ? "dark" : "light";
    }
    
      media.addEventListener("change", onThemeChange);
      onThemeChange();

}
</script>
