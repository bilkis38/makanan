<template>
  <div class="home">
    <NavbarWa />
    <div class="container">
      <HeroWa />

      <div class="row mt-4">
        <div class="col">
          <h2>Best <strong> FoodsView </strong></h2>
        </div>
        <router-link to="/FoodsView" class="btn btn-successs float-right"
          ><b-icon-eye></b-icon-eye>Lihat Semua
        </router-link>
      </div>
    </div>

    <div class="row mb-3">
      <div class="col-md-3 mt-4">
        <CardProductWa />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarWa from "@/components/NavbarWa.vue";
import HeroWa from "@/components/HeroWa.vue";
import CardProductWa from "@/components/CardProductWa.vue";
import axios from "axios";

export default {
  name: "HomeView",
  components: {
    NavbarWa,
    HeroWa,
    CardProductWa,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.product = data;
    },
  },
  mounted() {
    axios
      .get("https://localhost:3000/best-products")
      .then(function (response) {
        // handle success
        console.log("Berhasil : ", response);
      })
      .catch(function (error) {
        // handle error
        console.log("Gagal :", error );
      })
  },
};
</script>
