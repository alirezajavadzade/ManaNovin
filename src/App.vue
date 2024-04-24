<template>
  <v-app>
    <v-main>
      <v-app-bar :elevation="2">
        <v-app-bar-title>Mana Novin</v-app-bar-title>
        <RouterLink to="/AboutProject" class="nav-link">about project</RouterLink>
        <RouterLink to="/" class="nav-link">home</RouterLink>
      </v-app-bar>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts" setup>
//
</script>

<style>
.nav-link {
  margin: 0 1rem;
  text-decoration: none;
  color: #000;
  font-weight: 500;
}

.nav-link:hover {
  color: #5a5a5a;
}
</style>
