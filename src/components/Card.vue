<template>
  <div class="card">
    <div class="heading">
      <h2>{{ animal.name }}</h2>
      <i class="fas fa-fish fa-2x"></i>
    </div>
    <div class="img-container">
      <img class="img" :src="animal.img" alt="clownfish">
    </div>
    <div class="content-container">
      <div class="fact">{{ animal.fact }}</div>
      <ul class="details-list">
        <li v-for="(detail, name) in animal.details" :key="detail.name">
          <b>{{ name }}</b>
          :
          {{ detail }}
        </li>
      </ul>

      <div class="description">{{ animal.description }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",
  props: ["animal"]
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
