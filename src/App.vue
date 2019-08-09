<template>
  <div id="app">
    <textBlock v-bind:textHeader="myJson.name"/>
    <ul class="product-grid">
   <productCard
    v-for="data in myJson.groups"
    v-bind:key="data.groups"
    v-bind:productTitle="data.name"
    v-bind:id="data.id"
    v-bind:productUrl="data.links.www"
    v-bind:productimgUrl="data.hero.href"
    v-bind:productimgUrlAlt="data.images[0].href"
    v-bind:lowPrice="data.priceRange.selling.low"
    v-bind:highPrice="data.priceRange.selling.high"/>
  </ul>
  </div>
</template>

<script>
import productCard from './components/productGridItem.vue'
import textBlock from './components/textBlock.vue'
import json from './json/data.json'

export default {
  name: 'app',
  data(){
              return{
                  myJson: json
              }
  },
  components: {
    productCard,
    textBlock
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap');

.product-grid {
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap:wrap;
  max-width: 1108px;
  margin: 0 auto;
  padding-left:0;
}

 h1,h2,h3,h4,h5,p{
    font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  }

  h1,h2,h3,h4,h5{
    font-weight:700;
  }

  p{
    font-weight:400;
  }
</style>
