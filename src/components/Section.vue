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
      <li v-for="(link, index) in links" :key="index">
        <a v-bind:href="link.link" target="_blank">{{ link.title }}</a>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.box {
  display: flex;
  flex-flow: row wrap;
  padding: 5vh 0 5vw 0;
  color: #fbf1c7;
  transition: all 0.2s;
  width: 90vw;
  .info {
    padding: 0 10vw;
    width: 10vw;
  }
  .links {
    transition: all 0.5s ease-out;
    display: none;
    list-style: none;
    text-align: center;
  }
  .links > li {
    padding: 0 2vw;
    a {
      font-weight: bolder;
      text-decoration: none;
      color: #b8bb26;
    }
  }
  h3 {
    font-size: 2.5rem;
  }
  h6 {
    font-size: 0.9rem;
  }
  &:hover {
    padding-left: 2vw;
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

  @media (max-width: 700px) {
    padding: 8vh 5vw;
    .info {
      padding-left: 20vw;
      width: 100vw;
    }
  }
}
</style>
