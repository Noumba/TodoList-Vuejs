<script setup>
import { ref } from "vue";

const newTask = ref("");
const todoList = ref([
  {
    task: "Implementation of a todoList with Vue js",
    status: "Not Started",
    started: false,
    completed: false,
  },
  {
    task: "Implementation of a Simple Ecommerce page with Vue js",
    status: "Not Started",
    started: false,
    completed: false,
  },
  {
    task: "Implementation of the profile page of the mytech1 mobile app with Flutter",
    status: "Not Started",
    started: false,
    completed: false,
  },
  {
    task: "Create the UI for the Simple Bank API and integrate with the backend",
    status: "Not Started",
    started: false,
    completed: false,
  },
]);

function addNewTodo() {
  const todo = {
    task: newTask.value,
    status: "Not started",
    started: false,
    completed: false,
  };
  console.log(newTask);
  todoList.value.push(todo);
  newTask.value = "";
}

function deleteTask(task) {
  todoList.value = todoList.value.filter((todo) => todo !== task);
}

function markStart(task) {
  todoList.value.map((todo) =>
    todo === task ? ((todo.started = true), (todo.status = "In Progress")) : false
  );
  console.log(todoList.value);
}

function markCompleted(task) {
  todoList.value.map((todo) =>
    todo === task ? ((todo.completed = true), (todo.status = "Completed")) : false
  );
}
</script>

<template>
  <header><p class="mt-5 text-center text-uppercase fs-2 fw-bold">Todo List</p></header>
  <form @submit.prevent="addNewTodo">
    <div class="container d-flex justify-content-center">
      <input
        v-model="newTask"
        class="form-control w-75 p-3 border-2 rounded-3"
        type="text"
        placeholder="Enter Task"
      />
      <button class="btn btn-success">ADD TASK</button>
    </div>
  </form>
  <div class="container d-flex justify-content-center mt-5 w-100">
    <table class="table table-striped table-bordered table-responsive">
      <thead class="table-primary">
        <tr class="text-center">
          <th scope="col">#</th>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th>Start</th>
          <th>Completed</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody class="text-center">
        <tr class="" v-for="(todo, index) in todoList" :key="index">
          <td>{{ index + 1 }}</td>
          <td class="text-start" :class="{ completed: todo.completed }">
            {{ todo.task }}
          </td>
          <td>{{ todo.status }}</td>
          <td>
            <input
              @click="markStart(todo)"
              type="checkbox"
              v-model="todo.started"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <input
              @click="markCompleted(todo)"
              type="checkbox"
              v-model="todo.completed"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <div class="d-flex justify-content-around">
              <span class="fa fa-edit"></span
              ><span @click="deleteTask(todo)" class="fa fa-trash-can"></span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
table,
tbody,
tr,
td {
  padding: 15px;
}
table,
thead,
tr,
th {
  font-weight: 700;
  font-size: 20px;
  padding: 10px;
}
.completed {
  text-decoration: line-through;
}
</style>
