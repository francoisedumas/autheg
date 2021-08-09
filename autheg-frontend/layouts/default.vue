<template>
  <div id="app">
    <v-app>
      <v-app-bar app dark>
        <v-app-bar-title>Auth example</v-app-bar-title>
        <v-spacer />
        <v-btn icon nuxt href="/"><v-icon>home</v-icon></v-btn>
      </v-app-bar>
      <v-main>
        <v-container fluid>
          <nuxt/>
        </v-container>
      </v-main>
    </v-app>
  </div>
</template>