<script setup>
import Kategori from "@/assets/Kategori";
</script>

<template>
  <div class="hello">
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container">
        <a class="navbar-brand" href="">
          <img src="/img/logo_small.png" alt="" width="140" height="35" />
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
              <a class="nav-link active text-dark" href=""><router-link to="/">HOME</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href=""><router-link to="/about">PRODUCT</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href=""><router-link to="/login">LOGIN</router-link></a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="container-fluid header">
      <div class="position-relative p-3 p-md-5 text-center prod">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
          <img src="/img/men/kemeja-orang/Garment-Dyed_Oxford_Shirt.png" alt="" class="men" />
          <img src="/img/women/photo1661039990__1_-removebg-preview.png" alt="" class="women" />
          <h1 class="display-2 fw-normal">BALENDA</h1>
          <h6 class="fw-italic">Solution for your outfit of the day</h6>
          <!-- <p class="new-collection">NEW COLLECTION</p> -->
          <!-- <a class="btn btn-outline-secondary" href="#">Coming soon</a> -->
        </div>
        <div class="product-device shadow-sm d-none d-md-block"></div>
        <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
      </div>
      <section id="product">
        <div class="container p-3 p-md-5 text-center prod">
          <div class="row">
            <h3>Product Recommendation</h3>
            <div class="col mt-4" v-for="data in Kategori" :key="data">
              <div class="card">
                <router-link to="/about"><img :src="data.image" class="card-img-top gambar" alt="..." /></router-link>
                <div class="card-body text-center">
                  <h5 class="card-title title-name">{{ data.nama }}</h5>
                  <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <div class="container p-3 p-md-5 text-center prod">
        <div class="row">
          <h3>Product Recommendation</h3>
          <div class="col mt-4" v-for="data in Kategori" :key="data">
            <div class="card">
              <router-link to="/about"><img :src="data.image" class="card-img-top gambar" alt="..." /></router-link>
              <div class="card-body text-center">
                <h5 class="card-title title-name">{{ data.nama }}</h5>
                <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
              </div>
            </div>
          </div>
        </div>
      </div>
      <section id="footer">
        <div class="container-fluid footer">
          <footer class="py-5">
            <div class="row">
              <div class="col-7 col-md-3 mb-3">
                <h6>CONTACT US</h6>
                <ul class="nav flex-column">
                  <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-muted">balenda@gmail.com</a></li>
                  <li class="nav-item mb-2"><a href="#" class="nav-link p-0 text-muted">+62 9522 98741</a></li>
                  <li class="nav-item mb-2">Monday - Saturday: 10:00 am to 5pm (WIB)</li>
                </ul>
              </div>
              <div class="col-6 col-md-2 mb-3 gakpake">
                <h5>Section</h5>
                <ul class="nav flex-column">
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                </ul>
              </div>
              <div class="col-6 col-md-2 mb-3 gakpake">
                <h5>Section</h5>
                <ul class="nav flex-column">
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                  <li class="nav-item mb-2"></li>
                </ul>
              </div>
              <div class="col-md-4 offset-md-1 mb-3">
                <form>
                  <h5>Subscribe to our newsletter</h5>
                  <p>Monthly digest of what's new and exciting from us.</p>
                  <div class="d-flex flex-column flex-sm-row w-100 gap-2">
                    <label for="newsletter1" class="visually-hidden">Email address</label>
                    <input id="newsletter1" type="text" class="form-control" placeholder="Email address" />
                    <button class="btn btn-primary" type="button">Subscribe</button>
                  </div>
                </form>
              </div>
            </div>

            <div>
              <p>&copy; 2022 Balenda, Inc. All rights reserved.</p>
            </div>
          </footer>
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
.footer {
  background-color: white;
}
.gakpake {
  color: white;
}
.card {
  width: 14.4rem;
}
</style>