<script lang="ts" setup>
import { defineProps } from "vue";

defineProps<{
  title: string;
}>();
</script>

<template>
  <div class="container-bordered">{{ $props.title }}</div>
</template>

<style lang="scss" scoped>
.container-bordered {
  display: flex;
  flex-direction: column;
  padding: 10px;
  max-width: 400px;
  width: 90%;

  border: 1px solid #ddd;
  border-radius: 5px;

  text-align: left;
}
</style>
