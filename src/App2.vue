<script>
export default {
  data() {
    return {
      name: "John Doe",
      status: "active",
      tasks: ["Task 1", "Task 2", "Task 3"],
      link: "https://www.google.com",
    };
  },
  methods: {
    toggleStatus() {
      this.status = this.status === "active" ? "pending" : "active";
    },
  },
};
</script>

<template>
  <h1>Hello {{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is unknown</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <!-- <a v-bind:href="link">Google</a> -->
  <a v-bind:href="link">Google</a>

  <!-- <button v-on:click="toggleStatus">Greet</button> -->
  <button @click="toggleStatus">Greet</button>
</template>
