<template>
    <div id="app" class="container">
            <h1  class="green">Task Manager</h1>
            <div>
                <task-form @task-added="addTask"></task-form>
                <task-list :tasks="tasks"></task-list>
            </div>
    </div>
</template>
  
  <script>
    import TaskForm from '../components/TaskForm.vue';
    import TaskList from '../components/TaskList.vue';
  
    export default {
      components: {
        TaskForm,
        TaskList
      },
      data() {
        return {
          tasks: []
        };
      },
      methods: {
        addTask(newTask) {
          this.tasks.push(newTask);
        }
      }
    };
  </script>
  <style>
    .container {
        min-width: 100%;
       
        background-color: #fff;
        border-radius: 8px;
        box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
    }
  </style>