<script setup>
import Section from "./Section.vue";
</script>

<template>
  <div class="container">
    <Section title="Productivity" lorem="Only Apps" />
    <Section title="Cool stuff" lorem="Downtime and Media" />
    <Section title="Entertaiment" lorem="Files, Videos, Stream" />
    <Section title="Ref" lorem="Docs, Code + Specs" />
  </div>
</template>

<style lang="scss" scoped>
.container {
  height: 100vh;
  width: 35vw;
  background: #1d20213d;
  backdrop-filter: blur(20px);
  color: #fbf1c7;
  display: flex;
  flex-flow: column nowrap;
  justify-content: space-between;
  align-items: flex-end;
}
</style>
