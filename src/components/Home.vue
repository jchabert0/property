<template>
  <div class="home">
    <Navbar></Navbar>
    <Header></Header>

    <section class="section">
      <svg class="svg-icon box" viewBox="0 0 20 20">
        <path
          fill="#ff8c3b"
          d="M15.971,7.708l-4.763-4.712c-0.644-0.644-1.769-0.642-2.41-0.002L3.99,7.755C3.98,7.764,3.972,7.773,3.962,7.783C3.511,8.179,3.253,8.74,3.253,9.338v6.07c0,1.146,0.932,2.078,2.078,2.078h9.338c1.146,0,2.078-0.932,2.078-2.078v-6.07c0-0.529-0.205-1.037-0.57-1.421C16.129,7.83,16.058,7.758,15.971,7.708z M15.68,15.408c0,0.559-0.453,1.012-1.011,1.012h-4.318c0.04-0.076,0.096-0.143,0.096-0.232v-3.311c0-0.295-0.239-0.533-0.533-0.533c-0.295,0-0.534,0.238-0.534,0.533v3.311c0,0.09,0.057,0.156,0.096,0.232H5.331c-0.557,0-1.01-0.453-1.01-1.012v-6.07c0-0.305,0.141-0.591,0.386-0.787c0.039-0.03,0.073-0.066,0.1-0.104L9.55,3.75c0.242-0.239,0.665-0.24,0.906,0.002l4.786,4.735c0.024,0.033,0.053,0.063,0.084,0.09c0.228,0.196,0.354,0.466,0.354,0.76V15.408z"
        />
      </svg>
    </section>

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
    Header
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
.svg-icon {
  position: absolute;
  height: 250px;
  width: 250px;
  top: 360px;
  left: 5%;
  border-radius: 50%;
  padding: 10px;
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
