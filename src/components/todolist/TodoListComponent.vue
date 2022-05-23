<template>
  <header><p class="mt-5 text-center text-uppercase fs-2 fw-bold">Todo List</p></header>
  <div class="container d-flex justify-content-center">
    <input
      class="form-control w-75 p-3 border-2 rounded-3"
      type="text"
      placeholder="Enter Task"
    />
    <button class="btn btn-success">ADD TASK</button>
  </div>
  <div class="container d-flex justify-content-center mt-5 w-100 table-responsive">
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
        <tr>
          <td>1</td>
          <td>Python online class</td>
          <td>In Progress</td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <div class="d-flex justify-content-around">
              <span class="fa fa-edit"></span><span class="fa fa-trash-can"></span>
            </div>
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>Python online class</td>
          <td>In Progress</td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <div class="d-flex justify-content-around">
              <span class="fa fa-edit"></span><span class="fa fa-trash-can"></span>
            </div>
          </td>
        </tr>
        <tr>
          <td>3</td>
          <td>Python online class</td>
          <td>In Progress</td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <div class="d-flex justify-content-around">
              <span class="fa fa-edit"></span><span class="fa fa-trash-can"></span>
            </div>
          </td>
        </tr>
        <tr>
          <td>4</td>
          <td>Python online class</td>
          <td>In Progress</td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <input
              type="checkbox"
              class="form-check-input"
              name=""
              id=""
              value="checkedValue"
            />
          </td>
          <td>
            <div class="d-flex justify-content-around">
              <span class="fa fa-edit"></span><span class="fa fa-trash-can"></span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup></script>

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
</style>
