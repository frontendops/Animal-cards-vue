<template>
  <div id="app">
    <BaseModal v-if="showModal" @close="toggleModal"/>
    <Card v-for="animal in animals" :key="animal.fact" :animal="animal" v-on:open="toggleModal"/>
  </div>
</template>

<script>
import Card from "./components/Card.vue";
import BaseModal from "./components/BaseModal.vue";
export default {
  name: "app",
  components: {
    Card,
    BaseModal
  },
  data: function() {
    return {
      showModal: false,
      animals: [
        {
          name: "Clownfish",
          img:
            "https://images.unsplash.com/photo-1544552866-d3ed42536cfd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2251&q=80",
          fact:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, fuga. Dolores alias vel quo",
          details: [
            {
              label: "Scientific Name",
              value: "Amphriprotine"
            },
            {
              label: "Average Length",
              value: 11
            },
            {
              label: "Average Lifepan",
              value: "7 years"
            },
            {
              label: "Habitat",
              value: "Tropical Coral reef"
            }
          ],
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae maiores eaque adipisci dolor deleniti voluptate iste quia, nostrum tenetur consectetur ab tempore quaerat quo. Ratione dolorem temporibus delectus ipsa perspiciatis."
        },
        {
          name: "Dog",
          img:
            "https://images.unsplash.com/photo-1453227588063-bb302b62f50b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2250&q=80://images.unsplash.com/photo-1544552866-d3ed42536cfd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2251&q=80",
          fact:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, fuga. Dolores alias vel quo",
          details: [
            {
              label: "Scientific Name",
              value: "doggy"
            },
            {
              label: "Average Length",
              value: 45
            },
            {
              label: "Average Lifepan",
              value: "11 years"
            },
            {
              label: "Habitat",
              value: "Tropical Coral reef"
            }
          ],
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae maiores eaque adipisci dolor deleniti voluptate iste quia, nostrum tenetur consectetur ab tempore quaerat quo. Ratione dolorem temporibus delectus ipsa perspiciatis."
        }
      ]
    };
  },
  methods: {
    toggleModal: function() {
      this.showModal = !this.showModal;
    }
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
