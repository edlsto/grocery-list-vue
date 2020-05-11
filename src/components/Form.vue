<template>
  <div class="form">
    <div class="title input-item">
      <p>Title</p>
      <input type="text" v-model="title" />
    </div>
    <div class="description input-item">
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

input {
  height: 50px;
  font-size: 2em;
  outline: none;
  padding: 0.2em;
  width: 100%;
}

.input-item {
  width: 20em;
  margin-right: 1em;
}

.title {
  width: 15em;
}

.description {
  width: 30em;
}

.form {
  display: flex;
  justify-content: center;
}

button {
  height: 50px;
  font-size: 16px;
  align-self: flex-end;
  padding: 0.5em;
  width: 5em;
  cursor: pointer;
}

p {
  margin: 1em;
}
</style>
