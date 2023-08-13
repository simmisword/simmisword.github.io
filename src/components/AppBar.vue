<template>
  <v-app-bar scroll-behavior="hide">
    <v-app-bar-title>
      Hi, I am Simon
    </v-app-bar-title>
    <v-btn icon>
      <v-icon icon="mdi-room-service-outline"></v-icon>
      <v-menu activator="parent">
        <v-list>
          <v-list-item href="mailto:sschwertner23@gmail.com">
            <template v-slot:prepend>
              <v-icon icon="mdi-mail"></v-icon>
            </template>
            <v-list-item-title>E-Mail</v-list-item-title>
          </v-list-item>
          <v-list-item href="https://www.linkedin.com/in/simon-schwertner-0b5766200/">
            <template v-slot:prepend>
              <v-icon icon="mdi-linkedin"></v-icon>
            </template>
            <v-list-item-title>LinkedIn</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-btn>
  </v-app-bar>
</template>

<script setup>
  //
</script>
