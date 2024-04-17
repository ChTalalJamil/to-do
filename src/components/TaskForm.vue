<!-- TaskForm.vue -->
<template>
    <div >
        <form @submit.prevent="addTask" class="task-form">
              <input type="text" id="taskInput" v-model="newTask" placeholder="Add a new task">
              <button type="submit" >+</button>
        </form>
    </div>
   
</template>
  
  <script>
  export default {
    data() {
      return {
        newTask: ''
      };
    },
    methods: {
      addTask() {
        if (this.newTask.trim() !== '') {
          this.$emit('task-added', this.newTask.trim());
          this.newTask = '';
        }
      }
    }
  };
  </script>
  
<style scoped>
    .task-form {
      display: flex;
      justify-content: space-between;
    }   

    .task-form input {
      flex: 1;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    .task-form button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #41b883;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
    }

    .task-form button:hover {
    background-color: #45a049;
    }
    
</style>