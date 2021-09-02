<template>
  <h1>Jobs page</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h3>{{ job.title }}</h3>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { id: 1, title: "UX Designer", details: "Lorem" },
        { id: 2, title: "React Developer", details: "Lorem" },
        { id: 3, title: "Vue Developer", details: "Lorem" },
      ],
    };
  },
};
</script>

<style>
</style>