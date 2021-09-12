<template>
  <div class="container-list">
    <div class="no-tasks" v-if="tasks === undefined || tasks.length < 1">
      No Tasks, Add One 👻
    </div>
    <div class="task" v-for="task in tasks" :key="task.id">
      <div class="task-title">
        {{ task.title }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

interface Props {
  tasks: Task[];
}

type Task = {
  id: number;
  title: string;
  description?: string;
  completed?: boolean;
};

defineProps<Props>();
</script>

<style lang="scss" scoped>
.container-list {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  gap: 5px;
  .no-tasks {
    margin-block: 2rem;
    font-weight: bold;
  }
  .task {
    border: 1px solid #ddd;
    padding: 0.5rem;
    border-radius: 0.25rem;
    width: calc(100% - 20px);
    .task-title {
      font-weight: bold;
    }
  }
}
</style>
