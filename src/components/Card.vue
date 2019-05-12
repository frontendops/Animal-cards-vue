<template>
  <div class="card">
    <div class="heading">
      <h2>{{ animal }}</h2>
      <i class="fas fa-fish fa-2x"></i>
    </div>
    <div class="img-container">
      <img class="img" :src="img" alt="clownfish">
    </div>
    <div class="content-container">
      <div class="fact">{{ fact }}</div>
      <ul class="details-list">
        <li v-for="(detail, name) in details" :key="detail.name">
          <b>{{ name }}</b>
          :
          {{ detail }}
        </li>
      </ul>

      <div class="description">{{ description }}</div>
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
      description:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae maiores eaque adipisci dolor deleniti voluptate iste quia, nostrum tenetur consectetur ab tempore quaerat quo. Ratione dolorem temporibus delectus ipsa perspiciatis."
    };
  }
};
</script>

<style scoped>
.card {
  max-width: 400px;
  margin: 50px auto;
  border-radius: 10px;
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
  display: flex;
  flex-direction: column;
}

.heading {
  text-align: left;
  padding: 0px 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.img-container {
  margin: 0px 10px 10px 10px;
}
.img {
  width: 100%;
  align-self: center;
}

.content-container {
  border: 1px solid gray;
  border-radius: 10px;
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

.description {
  padding: 10px;
}
</style>
