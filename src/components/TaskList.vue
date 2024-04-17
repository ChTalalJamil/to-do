<template>
    <div>
        <ul class="task-list">
          <li style="list-style-type: square;" v-for="(task, index) in tasks" :key="index" class="task-item">{{ task }}</li>
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
    padding: 0;
    }

    .task-item {
    padding: 10px;
    margin: 2%;
    background-color: #565353;
    border-radius: 4px;
    /* color: ; */
    }
</style>