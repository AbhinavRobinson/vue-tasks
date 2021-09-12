<template>
  <div class="home">
    <Container title="Vue Tasks">
      <Tasklist
        :tasks="[{ id: 0, title: `Complete this app!`, completed: true }]"
      />
    </Container>
  </div>
</template>

<script lang="ts" setup>
import Container from "@/components/Container.vue";
import Tasklist from "@/components/Tasklist.vue";
</script>

<style lang="scss" scoped>
.home {
  display: grid;
  place-items: center;
}
</style>
