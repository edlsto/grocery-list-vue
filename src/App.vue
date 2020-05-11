<template>
  <div id="app">
    <h1>My shopping list</h1>
    <Form v-on:submit-title="submitItem"></Form>
    <CardContainer :items="items" />
  </div>
</template>

<script>
import CardContainer from "./components/CardContainer.vue";
import Form from "./components/Form.vue";

export default {
  components: {
    CardContainer,
    Form
  },
  name: "app",
  data() {
    return {
      items: []
    };
  },
  methods: {
    submitItem: function(event) {
      this.items.push(event);
    }
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 1000px;
  margin: 5em auto;
}

h1,
h2 {
  font-weight: normal;
}

h1 {
  margin-bottom: 1em;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
