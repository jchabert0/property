<template>
  <div class="home">
    <Navbar></Navbar>
    <Header></Header>
    <Logo></Logo>
    <About></About>

    <section class="section" id="properties">
      <div class="container">
        <div class="columns is-vcentered is-centered">
          <div class="column" v-for="(property, index) in properties" :key="index">
            <div class="box" :style="{ 'background-image': 'url(' + property.image + ')' }">
              <h1 class="title">{{ property.title }}</h1>
              <h2 class="subtitle">{{ property.description }}</h2>
              <button class="button is-primary" @click="goTodetail(property.id)">button</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <Footer></Footer>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";
import Header from "./Header.vue";
import Logo from "./Logo.vue";
import About from "./About.vue";
import Footer from "./Footer.vue";

export default {
  name: "Home",
  data() {
    return {
      properties: [
        {
          id: 1,
          title: "property-1",
          description: "description",
          image: "../assets/img-property-4.jpg"
        },
        {
          id: 2,
          title: "property-2",
          description: "description",
          image: "../assets/img-property-4.jpg"
        },
        {
          id: 3,
          title: "property-3",
          description: "description",
          image: "../assets/img-property-4.jpg"
        }
      ]
    };
  },
  components: {
    Navbar,
    Header,
    Logo,
    About,
    Footer
  },
  methods: {
    goTodetail(propertyId) {
      this.$router.push({ name: "Property", params: { id: propertyId } });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
