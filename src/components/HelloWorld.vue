<script setup>
import Kategori from "@/assets/Kategori";
</script>

<template>
  <div class="hello">
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container">
        <a class="navbar-brand" href="">
          <img src="../assets/img/logo_small.png" alt="" width="140" height="35" />
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link text-dark" href="#">SHOP</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href="">REVIEW</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active text-dark" href="">HOME</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href=""><router-link to="/about">PRODUCT</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href="">CONTACT US</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="container-fluid header">
      <div class="position-relative p-3 p-md-5 m-md-3 text-center prod">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
          <img src="../assets/img/men/kemeja-orang/Garment-Dyed_Oxford_Shirt.png" alt="" class="men" />
          <img src="../assets/img/women/photo1661039990__1_-removebg-preview.png" alt="" class="women" />
          <h1 class="display-2 fw-normal">BALENDA</h1>
          <h6 class="fw-italic">Solution for your outfit of the day</h6>
          <!-- <p class="new-collection">NEW COLLECTION</p> -->
          <!-- <a class="btn btn-outline-secondary" href="#">Coming soon</a> -->
        </div>
        <div class="product-device shadow-sm d-none d-md-block"></div>
        <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
      </div>
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
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data: function () {
    return {
      // kategori: [
      //   {
      //     nama: "WOMEN'S",
      //     image: "https://images.unsplash.com/photo-1427348693976-99e4aca06bb9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dmlzaW9ufGVufDB8fDB8fA%3D%3D&w=1000&q=80",
      //   },
      //   {
      //     nama: "ACCESORIES",
      //     image: "https://images.unsplash.com/photo-1427348693976-99e4aca06bb9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dmlzaW9ufGVufDB8fDB8fA%3D%3D&w=1000&q=80",
      //   },
      //   {
      //     nama: "MEN'S",
      //     image: "https://images.unsplash.com/photo-1501139083538-0139583c060f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dGltZXxlbnwwfHwwfHw%3D&w=1000&q=80",
      //   },
      // ],
    };
  },
  // methods: {
  //   changeTitle(data) {
  //     this.titleHero = data.;
  //     this.titleImage = data.image;
  //   },
  // },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.men {
  position: absolute;
  left: 60px;
  width: 300px;
  top: 100px;
}
.women {
  position: absolute;
  right: 40px;
  width: 370px;
  top: 0px;
}
.prod {
  position: relative;
  background-color: #dcd7c9;
  height: 499px;
}
.new-collection {
  position: absolute;
  left: 30px;
  width: 300px;
  top: 50px;
  font-size: 40px;
  float: left;
}
.header {
  background-color: #dcd7c9;
  left: 100px;
}
</style>
