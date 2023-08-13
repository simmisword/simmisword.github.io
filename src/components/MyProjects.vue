<template>
  <v-row class="ma-0">
    <v-col class="pa-0" cols="6" v-for="project in projects" :key="project.name">
      <Project :name="project.name" :subtitle="project.subtitle" :url="project.coverURL" />
    </v-col>
  </v-row>
</template>

<script setup>
import projects from "@/store/projects"
import Project from '@/components/Project.vue'


</script>
