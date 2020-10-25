<template>
  <div class="main">
    <div
      v-for="page in pages"
      :key="page.page"
      class="page"
      :style="{
        top: `${page.x1}px`,
        left: `${page.y1}px`,
        height: `${page.x2 - page.x1}px`,
        width: `${page.y2 - page.y1}px`
      }"
    >
      {{ page.word }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pages: [
        {
          page: 1,
          x1: 207.41,
          y1: 159.10256,
          x2: 279.230512,
          y2: 173.69,
          word: "STATUTS"
        }
      ]
    };
  },
  methods: {},
  components: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
  background-color: azure;
  position: relative;
}
.page {
  position: absolute;
  border: 1px solid black;
}
</style>
