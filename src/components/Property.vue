<template>
  <div class="property">
    <h1>la propriété {{ this.$route.params.id }}</h1>
    <div v-for="(property,index) in properties" :key="index">
      <div v-if="propertyId == property.id">
        <h1>{{property.title}}</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Property',
  data () {
    return {
      propertyId: this.$route.params.id,
      property: 'Property page',
      properties: [
        { id: 1, title: 'property-1' },
        { id: 2, title: 'property-2' },
        { id: 3, title: 'property-3' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
