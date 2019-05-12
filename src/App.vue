<template>
  <div id="app">
    <Card :animal="animal"/>
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "app",
  components: {
    Card
  },
  data: function() {
    return {
      animal: {
        name: "Clownfish",
        img:
          "https://images.unsplash.com/photo-1544552866-d3ed42536cfd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2251&q=80",
        fact:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, fuga. Dolores alias vel quo",
        details: {
          "Scientific Name": "Amphipriotine",
          "Average length": "11 cm",
          "Average Lifespan": "7 years",
          Habitat: "Tropical Coral Reef"
        },
        description:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae maiores eaque adipisci dolor deleniti voluptate iste quia, nostrum tenetur consectetur ab tempore quaerat quo. Ratione dolorem temporibus delectus ipsa perspiciatis."
      }
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
