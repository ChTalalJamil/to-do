<template>
    <div>
        <ul class="task-list">
        <li v-for="(task, index) in tasks" :key="index" class="task-item">{{ task }}</li>
        </ul>
    </div>
</template>
  
  <script>
  export default {
    props: ['tasks']
  };
  </script>
  
<style scoped>
    .task-list {
    list-style: none;
    padding: 0;
    }

    .task-item {
    padding: 10px;
    margin-bottom: 5px;
    background-color: #f9f9f9;
    border-radius: 4px;
    }
</style>