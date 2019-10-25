<template>
  <div class="home">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="(property, index) in properties" :key="index">
        
        <a @click="goTodetail(property.id)">
        {{ property.id }}
         {{ property.title }}
          {{ property.img }}
        </a>
        
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Home page',
      properties: [
      { id: 1, title: 'property-1', img: 'img'},
      { id: 2, title: 'property-2', img: 'img'},
      { id: 3, title: 'property-3', img: 'img'},
    ]
    }
  },
  methods: {
 goTodetail(propertyId) {
    this.$router.push({name:'Property', params:{id: propertyId}})
  }
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
