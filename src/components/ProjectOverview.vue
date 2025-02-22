<template>
  <div class="text-white p-5 text-center">
    <h2 class="text-2xl font-bold">Projects</h2>
    <ul>
      <li v-for="project in projects" :key="project.id">
        <h3 class="text-xl">{{ project.title }}</h3>
        <p>{{ project.description }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
  import { ref, onMounted } from 'vue';
  import axios from 'axios';

  interface Project {
    id: number;
    title: string;
    description: string;
  }

  const projects = ref<Project[]>([]);

  onMounted(async () => {
    const response = await axios.get('http://localhost/api/projects');
    projects.value = response.data;
  });
</script>
