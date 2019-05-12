<template>
  <div class="card">
    <h2 class="heading">{{ animal }}</h2>
    <div class="img-container">
      <img class="img" :src="img" alt="clownfish">
    </div>
    <div class="content-container">
      <div class="fact">{{ fact }}</div>
      <ul class="details-list">
        <li v-for="(detail, name) in details">
          <b>{{ name }}</b>
          :
          {{ detail }}
        </li>
      </ul>
    </div>
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
      fact:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, fuga. Dolores alias vel quo",
      details: {
        "Scientific Name": "Amphipriotine",
        "Average length": "11 cm",
        "Average Lifespan": "7 years",
        Habitat: "Tropical Coral Reef"
      },
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

.heading {
  text-align: left;
  padding: 0px 10px;
}

.img-container {
  margin: 0px 10px 10px 10px;
}
.img {
  width: 100%;
  align-self: center;
}

.content-container {
  border: 1px solid black;
  margin: 0px 10px 10px 10px;
  text-align: left;
}

.fact {
  font-style: italic;
  padding: 10px;
}

.details-list {
  list-style: none;
  padding-left: 10px;
}
</style>
