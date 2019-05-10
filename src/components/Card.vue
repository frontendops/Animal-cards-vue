<template>
  <div class="card">
    <h2 class="heading">{{animal}}</h2>
    <img class="img" :src="img" alt="clownfish">
    <div class="content-container"></div>
  </div>
</template>

<script>
export default {
  name: "card",
  data: function() {
    return {
      animal: "Clownfish",
      img:
        "https://images.unsplash.com/photo-1544552866-d3ed42536cfd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2251&q=80",
      description: "a fish from finding nemo"
    };
  }
};
</script>

<style scoped>
.card {
  max-width: 400px;
  margin: 0 auto;
  border: 1px solid black;
  display: flex;
  flex-direction: column;
}

.img {
  width: 90%;
  align-self: center;
}
</style>

