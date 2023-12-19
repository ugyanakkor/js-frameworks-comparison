<script setup lang="ts">
  const {data: nuxt_repo} = await useFetch('https://api.github.com/repos/nuxt/nuxt');
  const {data: angular_repo} = await
    useFetch('https://api.github.com/repos/angular/angular');
</script>

<template>
  <div>
    Nuxt stars: <span>{{nuxt_repo?.stargazers_count}}</span>
  </div>
  <div>
    Angular stars: <span>{{angular_repo.stargazers_count}}</span>
  </div>
</template>