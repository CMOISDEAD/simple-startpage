<script>
export default {
  props: {
    title: String,
    lorem: String,
    links: Array,
  },
};
</script>

<template>
  <div class="box">
    <div class="info">
      <h3 class="title">{{ title }}</h3>
      <h6 class="lorem">{{ lorem }}</h6>
    </div>
    <ul class="links">
      <li v-for="(link, index) in links" :key="index">{{ link }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.box {
  display: flex;
  flex-flow: row nowrap;
  padding: 5vh 5vw;
  text-align: right;
  color: #fbf1c7;
  transition: all 0.2s;

  .links {
    display: none;
    list-style: none;
  }

  h3 {
    font-size: 2.5rem;
  }

  h6 {
    font-size: 0.9rem;
  }

  &:hover {
    padding: 6vh 6vw;

    .lorem {
      color: #548588;
    }

    .links {
      display: block;
      li {
        display: inline-block;
      }
    }
  }
}
</style>
