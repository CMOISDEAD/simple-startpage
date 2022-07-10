<script>
export default {
  props: {
    title: String,
    lorem: String,
  },
};
</script>

<template>
  <div class="box">
    <h3>{{ title }}</h3>
    <h6>{{ lorem }}</h6>
  </div>
</template>

<style lang="scss" scoped>
.box {
  padding: 5vh 5vw;
  text-align: right;
  color: #fbf1c7;
  transition: all 0.2s;

  h3 {
    font-size: 2.5rem;
  }
  h6 {
    font-size: 0.9rem;
  }

  &:hover {
    padding: 6vh 6vw;
  }
}
</style>
