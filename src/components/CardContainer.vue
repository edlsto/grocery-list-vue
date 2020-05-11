<template>
  <div class="card-container">
    <div class="item" v-for="item in items" :key="item.key">
      <card :title="item.title" :description="item.description"></card>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  components: {
    Card
  },
  name: "CardContainer",
  props: ["items"]
};
</script>

<style lang="scss" scoped>
.card-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  /* margin-top: 2em; */
  width: 80%;
  margin: 2em auto;
  grid-column-gap: 1em;
}
</style>
