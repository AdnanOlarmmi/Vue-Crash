<script setup>
import { ref, onMounted } from "vue";

const name = ref("John Doe");
const status = ref("active");
const tasks = ref(["Task 1", "Task 2", "Task 3"]);
const link = ref("https://www.google.com");
const newTask = ref("sdasdf");
const toggleStatus = () => {
  status.value = status.value === "active" ? "pending" : "active";
};

const addTask = () => {
  if (newTask.value.trim() !== "") {
    tasks.value.push(newTask.value);
    newTask.value = "";
  }
};

const deleteTask = (index) => {
  tasks.value.splice(index, 1);
};

onMounted(async () => {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/todos");
    const data = await response.json();
    tasks.value = data.map((item) => item.title);
  } catch (error) {
    console.error("Error fetching tasks:", error);
  }
});
</script>

<template>
  <h1>Hello {{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is unknown</p>

  <form @submit.prevent="addTask">
    <label for="newTask">Add Task</label>
    <input type="text" id="newTask" name="newTask" v-model="newTask" />
    <button type="submit">Add Task</button>
  </form>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="(task, index) in tasks" :key="task">
      <span>{{ task }}</span>

      <button @click="deleteTask(index)">Delete</button>
    </li>
  </ul>
  <!-- <a v-bind:href="link">Google</a> -->
  <a v-bind:href="link">Google</a>

  <!-- <button v-on:click="toggleStatus">Greet</button> -->
  <button @click="toggleStatus">Greet</button>
</template>

<!-- <script>
import { ref } from "vue";
export default {
  setup() {
    const name = ref("John Doe");
    const status = ref("active");
    const tasks = ref(["Task 1", "Task 2", "Task 3"]);
    const link = ref("https://www.google.com");
    const toggleStatus = () => {
      status.value = status.value === "active" ? "pending" : "active";
    };
    return {
      name,
      status,
      tasks,
      link,
      toggleStatus,
    };
  },
};
</script> -->
