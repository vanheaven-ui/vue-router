<template>
  <h1>Jobs page</h1>
  <div v-for="job in jobs" :key="job.id">
    <h3>{{ job.title }}</h3>
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