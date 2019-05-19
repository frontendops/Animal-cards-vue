<template>
  <ul class="details-list">
    <template v-for="detail in details">
      <slot :detail="detail"></slot>
    </template>
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
