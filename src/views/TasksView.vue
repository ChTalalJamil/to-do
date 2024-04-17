<template>
    <div id="container">
      <div>
        <h1  class="green">Task Manager</h1>
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
          this.tasks.unshift(newTask);
        }
      }
    };
  </script>