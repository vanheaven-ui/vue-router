<template>
  <h1>Jobs page</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
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
.job h3 {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}

.job h3:hover {
  background-color: #ddd;
}

.job a {
  text-decoration: none;
}
</style>