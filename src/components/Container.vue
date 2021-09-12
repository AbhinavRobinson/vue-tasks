<template>
  <div class="container-bordered">
    <div class="header">
      <h1 class="title">
        {{ $props.title }}
      </h1>
      <button>Add Tasks</button>
    </div>
    <slot />
  </div>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

defineProps<{
  title: string;
}>();
</script>

<style lang="scss" scoped>
.container-bordered {
  display: flex;
  flex-direction: column;
  padding: 10px 15px;
  max-width: 400px;
  width: 90%;
  gap: 5px;

  border: 1px solid #ddd;
  border-radius: 5px;

  text-align: left;

  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    .title {
      font-size: 1.25rem;
      line-height: 0.5rem;
    }
    button {
      border: 1px solid #ddd;
      padding: 5px 10px;
      border-radius: 5px;
      background-color: transparent;
      text-transform: uppercase;
      transition-duration: 300ms;
      &:hover {
        cursor: pointer;
        box-shadow: 0 2px 5px #86e9bc77;
      }
    }
  }
}
</style>
