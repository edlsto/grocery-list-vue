<template>
  <div class="item">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  props: ["title", "description"]
};
</script>

<style lang="scss" scoped>
.item {
  border: 1px solid black;
  padding: 1em;
}

h2 {
  margin-bottom: 0.5em;
}
</style>
