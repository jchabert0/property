<template>
  <div class="home">
    <Navbar></Navbar>
    <Header></Header>
    <Logo></Logo>

    <section class="section" id="about">
      <div class="container">
        <div class="columns is-vcentered">
          <div class="column">
            <p class="pitch-left">
              Lorem ipsum dolor sit amet
              <span class="text-style">consectetur adipisicing elit</span>. Sint eum illo et nihil ea necessitatibus dolor dignissimos provident sed recusandae vero, repudiandae
              <span
                class="text-style"
              >repellat nisi</span> quo ipsum quia nesciunt accusamus aspernatur!
            </p>
          </div>
          <div class="column">
            <div class="section-img-div">
              <figure class="image is-4by3 section-img section-img-right">
                <img src="../assets/img-property-3.jpg" />
              </figure>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns is-vcentered">
          <div class="column">
            <div class="section-img-div">
              <figure class="image is-4by3 section-img section-img-left">
                <img src="../assets/img-property-4.jpg" />
              </figure>
            </div>
          </div>
          <div class="column">
            <p class="pitch-right">
              Lorem ipsum
              <span class="text-style">dolor sit</span> amet consectetur adipisicing elit. Sint eum illo et nihil ea necessitatibus dolor
              <span
                class="text-style"
              >dignissimos provident sed recusandae</span> vero, repudiandae repellat nisi quo ipsum quia nesciunt accusamus aspernatur!
            </p>
          </div>
        </div>
      </div>
    </section>

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

    <footer class="footer" id="contact">
      <div class="content has-text-centered">
        <p>
          <strong>Site vitrine</strong> by
          <a href="https://jgthms.com">Jeremy Thomas</a>. The source code is licensed
          <a href="http://opensource.org/licenses/mit-license.php">MIT</a>. The website content
          is licensed
          <a
            href="http://creativecommons.org/licenses/by-nc-sa/4.0/"
          >CC BY NC SA 4.0</a>.
        </p>
      </div>
    </footer>
  </div>
</template>

<script>
import Navbar from "./Navbar.vue";
import Header from "./Header.vue";
import Logo from "./Logo.vue";

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
    Logo
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
.text-style {
  color: #ff8c3b;
  font-weight: bolder;
}

.section-img-div {
  background: #ff8c3b;
}
.section-img {
  opacity: 1;
  -webkit-transition: 0.3s ease-in-out;
  transition: 0.3s ease-in-out;
}
.section-img:hover {
  opacity: 0.7;
}
.section-img-right {
  box-shadow: -125px 40px 0px 0px rgba(255, 229, 210, 0.3);
  -webkit-box-shadow: -125px 40px 0px 0px rgba(255, 229, 210, 0.3);
  -moz-box-shadow: -125px 40px 0px 0px rgba(255, 229, 210, 0.3);
}
.section-img-left {
  box-shadow: 125px 40px 0px 0px rgba(255, 229, 210, 0.3);
  -webkit-box-shadow: 125px 40px 0px 0px rgba(255, 229, 210, 0.3);
  -moz-box-shadow: 125px 40px 0px 0px rgba(255, 229, 210, 0.3);
}
.pitch-left {
  padding: 10px;
  border-top: 2px solid #ffe5d2;
  border-left: 2px solid #ffe5d2;
}
.pitch-right {
  padding: 10px;
  border-bottom: 2px solid #ffe5d2;
  border-right: 2px solid #ffe5d2;
}
#contact {
  background-color: #ffe5d2;
}
</style>
