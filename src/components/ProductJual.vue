<script setup>
import Kategori from '@/assets/Kategori';
</script>
<template>
  <div class="produk">
    <section id="product">
      <div class="p-3 p-md-5 m-md-3 text-center prod">
        <div class="row">
          <h3>Product Recommendation</h3>
          <div class="col mt-4" v-for="data in Kategori" :key="data">
            <div class="card" style="width: 20rem">
              <img :src="data.image" class="card-img-top" alt="..." />
              <div class="card-body text-center">
                <h5 class="card-title title-name">{{ data.nama }}</h5>
                <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "ProductJual",
  props: {
    msg: String,
  },
};
</script>

<style></style>
