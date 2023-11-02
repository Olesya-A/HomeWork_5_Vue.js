<template>
  <div>
    <h3>Name - {{ product.name }}</h3>
    <h3>Price - {{ formattedPrice }}</h3>
    <h3>
      Availability -
      <span v-if="product.availabe">Availlable</span>
      <span v-else>Out of stock</span>
    </h3>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
  computed: {
    formattedPrice() {
      return `$${this.product.price}`;
    },
  },
};
</script>

<style lang="scss" scoped>
div {
  width: 300px;
  border: 1px solid #000;
  display: flex;
  flex-direction: column;
  padding-left: 20px;
}
</style>
