<template>
  <div>
    <ProductComponent
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
  </div>
</template>

<script>
import ProductComponent from "./ProductComponent.vue";

export default {
  data() {
    return {
      products: [
        {
          name: "iphone15",
          price: 199.99,
          availabe: false,
        },
        {
          name: "iphone13",
          price: 99.99,
          availabe: true,
        },
        {
          name: "iphone8",
          price: 39.99,
          availabe: false,
        },
      ],
    };
  },
  components: {
    ProductComponent,
  },
};
</script>

<style lang="scss" scoped>
div {
  display: flex;
  gap: 20px;
}
</style>
