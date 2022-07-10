<script>
import Section from "./Section.vue";

export default {
  name: "Sidebar",
  data() {
    return {
      dev: [
        {
          title: "Github",
          link: "https://github.com",
        },
        {
          title: "Stackoverflow",
          link: "https://stackoverflow.com",
        },
        {
          title: "Gitlab",
          link: "https://gitlab.com",
        },
        {
          title: "FreeCodeCamp",
          link: "https://freecodecamp.org",
        },
      ],
      media: [
        {
          title: "youtube",
          link: "https://youtube.com",
        },
        {
          title: "Cuevana",
          link: "https://Cuevana3.me",
        },
        {
          title: "Unixporn",
          link: "https://reddit.com/r/unixporn",
        },
        {
          title: "Reddit",
          link: "https://reddit.com",
        },
      ],
      social: [
        {
          title: "Instagram",
          link: "https://instagram.com",
        },
        {
          title: "Twitter",
          link: "https://twitter.com",
        },
      ],
      news: [
        {
          title: "Hacker News",
          link: "https://hackernews.org",
        },
        {
          title: "guardian",
          link: "https://guardian.com",
        },
      ],
    };
  },
  components: {
    Section,
  },
};
</script>

<template>
  <div class="sidebar">
    <Section title="Development" lorem="Only Apps" v-bind:links="dev" />
    <Section
      title="Entertaiment"
      lorem="Downtime and Media"
      v-bind:links="media"
    />
    <Section
      title="Social"
      lorem="Files, Videos, Stream"
      v-bind:links="social"
    />
    <Section title="News" lorem="Docs, Code + Specs" v-bind:links="news" />
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  z-index: 10;
  position: absolute;
  margin: 4vh 0;
}
</style>
