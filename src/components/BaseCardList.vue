<template>
  <ul class="details-list">
    <li v-for="detail in details" :key="detail.value">
      <slot :detail="detail"></slot>
    </li>
  </ul>
</template>

<script>
export default {
  name: "detailsList",
  props: {
    details: {
      type: Array
    }
  }
};
</script>

<style scoped>
</style>
