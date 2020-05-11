<template>
  <div class="form">
    <div class="title">
      <p>Title</p>
      <input type="text" v-model="title" />
    </div>
    <div class="description">
      <p>Description</p>
      <input type="text" v-model="description" />
    </div>
    <button v-on:click="$emit('submit-title', handleSubmit())">
      Submit
    </button>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      title: "",
      description: ""
    };
  },
  methods: {
    handleSubmit() {
      const newItem = { title: this.title, description: this.description };
      this.title = "";
      this.description = "";
      return newItem;
    }
  }
};
</script>

<style lang="scss" scoped>
.item {
  border: 1px solid black;
}
</style>
