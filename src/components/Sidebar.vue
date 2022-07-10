<script>
import Section from "./Section.vue";

export default {
  name: "Sidebar",
  data() {
    return {
      links: ["google.com", "cuevana.com", "devto.com", "reddit.com"],
    };
  },
  components: {
    Section,
  },
};
</script>

<template>
  <div class="container">
    <Section title="Productivity" lorem="Only Apps" v-bind:links="links" />
    <Section
      title="Cool stuff"
      lorem="Downtime and Media"
      v-bind:links="links"
    />
    <Section
      title="Entertaiment"
      lorem="Files, Videos, Stream"
      v-bind:links="links"
    />
    <Section title="Ref" lorem="Docs, Code + Specs" v-bind:links="links" />
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
