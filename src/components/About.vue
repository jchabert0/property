<template>
  <section class="section" id="about">
    <div class="container">
      <div class="columns is-vcentered">
        <div class="column">
          <div class="img-div">
            <figure class="image is-16by9 img">
              <img src="../assets/img-property-3.jpg" />
            </figure>
          </div>
        </div>
        <div class="column has-text-centered">
          <button class="button is-rounded">Contactez-nous</button>
          <!-- Réussir le hover qui change l'image -->
          <p class="text">
            Lorem ipsum
            <span>dolor sit</span> amet consectetur adipisicing elit. Sint eum illo et nihil ea necessitatibus dolor
            <span>dignissimos provident sed recusandae</span> vero, repudiandae repellat nisi quo ipsum quia nesciunt accusamus aspernatur!
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.button {
  font-weight: bold;
  border: none;
  margin-bottom: 20px;
  background-color: #ff8c3b;
  color: #ffffff;
}
.button:hover ~ .text {
  border-bottom: 2px solid #ffe5d2;
  border-right: 2px solid #ffe5d2;
  border-left: transparent;
  transform: translateX(-5px);
}
.button:hover ~ .img {
  -ms-transform: rotate(-3deg);
  -webkit-transform: rotate(-3deg);
  transform: rotate(-3deg);
  box-shadow: none;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
}
.text {
  padding: 10px;
  border-right: transparent;
  border-bottom: transparent;
  border-left: 2px solid #ffe5d2;
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
</style>
