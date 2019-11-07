<template>
  <section class="section" id="about">
    <div class="container">
      <div class="columns is-vcentered">
        <div class="column has-text-centered about-section">
          <div class="img-div">
            <figure class="image is-16by9 img" id="img">
              <img src="../assets/img-property-3.jpg" />
            </figure>
          </div>
          <button class="button is-rounded" id="btn-property" @mouseenter="mouseenter()" @mouseleave="mouseleave()">Découvrir nos biens</button>
        </div>
        <div class="column has-text-centered about-section">
          <button class="button is-rounded" id="btn-contact">Contactez-nous</button>
          <p class="text">
            Lorem ipsum 
            <span> dolor sit 
            </span> 
            amet consectetur adipisicing elit. Sint eum illo et nihil ea necessitatibus dolor 
            <span> 
            dignissimos provident sed recusandae
            </span> 
            vero, repudiandae repellat nisi quo ipsum quia nesciunt accusamus aspernatur!
            Lorem ipsum  dolor sit 
            <span> amet consectetur adipisicing
            </span> 
            elit. Sint eum illo et nihil ea necessitatibus dolor 
            <span> 
            dignissimos 
            </span> 
            provident sed recusandae vero, 
            <span>
              repudiandae
            </span> repellat nisi quo ipsum quia nesciunt accusamus aspernatur!
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {}
  },
  methods: {
    mouseenter () {
      document.getElementById('img').classList.add('img-hover')
    },
    mouseleave () {
      document.getElementById('img').classList.remove('img-hover')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.button {
  font-weight: bold;
  border: none;
  background-color: #ff8c3b;
  color: #ffffff;
  -webkit-box-shadow: 0px 3px 10px 0px rgb(194, 194, 194);
  -moz-box-shadow: 0px 3px 10px 0px rgb(194, 194, 194);
  box-shadow: 0px 3px 10px 0px rgb(194, 194, 194);
}
#btn-contact {
  margin-bottom: 20px;
}
#btn-property {
  margin-top: 42px;
}
#btn-contact:hover ~ .text {
  border-bottom: 2px solid #ffe5d2;
  border-right: 2px solid #ffe5d2;
  border-left: transparent;
  transform: translateX(-5px);
}
.text {
  background-color: #f8f8f8;
  padding: 10px;
  border-right: transparent;
  border-bottom: transparent;
  border-left: 4px solid #ffe5d2;
  -webkit-transition: 0.3s ease-in-out;
  transition: 0.3s ease-in-out;
}
span {
  color: #ff8c3b;
  font-weight: bolder;
}
.img-div {
  background: #ffe5d2;
}
.img {
  -webkit-transition: 0.3s ease-in-out;
  transition: 0.3s ease-in-out;
  box-shadow: 12px 12px 0px 0px #ffe5d2;
  -webkit-box-shadow: 12px 12px 0px 0px #ffe5d2;
  -moz-box-shadow: 12px 12px 0px 0px #ffe5d2;
}
.img-hover {
  -ms-transform: rotate(-3deg);
  -webkit-transform: rotate(-3deg);
  transform: rotate(-3deg);
  box-shadow: none;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
}
.about-section {
  margin-top: 3rem;
}
</style>
