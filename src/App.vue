<template>
  <div class="flex w-full">
    <div class="w-1/2">
      <HomeView />
    </div>
    <div class="w-1/2 flex justify-center items-center">
      <ProjectOverview />
    </div>
  </div>
</template>

<script setup lang="ts">
  import HomeView from '@/components/HomeView.vue'
  import ProjectOverview from '@/components/ProjectOverview.vue'
</script>
