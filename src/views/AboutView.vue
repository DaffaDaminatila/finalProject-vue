<template>
  <div class="about">
    <router-link to="/">sadas</router-link>
  </div>
  <ProductJual />
</template>

<script>
import ProductJual from "@/components/ProductJual.vue";
export default {
  name: "AboutView",
  components: { ProductJual },
};
</script>
