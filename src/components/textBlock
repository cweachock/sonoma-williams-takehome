<template>
<li itemprop="itemListElement" itemscope itemtype="http://schema.org/ListItem" class="product-grid-item">
  <div :id="productId" itemprop="item" itemscope itemtype="http://schema.org/Product">
    <a :href="productUrl" :title="productTitle" >
    <img :src="productimgUrl" :alt="productTitle" itemprop="image" class="product-grid-item-img">
    <img :src="productimgUrlAlt" :alt="productTitle" itemprop="image" class="product-grid-item-img">
    <h1 class="product-grid-item-title" itemprop="name" v-html="productTitle"></h1>
    <div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <meta itemprop="priceCurrency" content="USD">
    <p class="product-grid-item-price">
        from $<span itemprop="lowPrice">{{lowPrice}}</span> to $<span itemprop="highPrice">{{highPrice}}</span></p>
    </div>
    </a>
  </div>
  </li>
</template>

<script>

export default {
  name: 'productCard',
  props: {
    productTitle: String,
    productId: String,
    productUrl: String,
    productimgUrl: String,
    productimgUrlAlt: String,
    lowPrice: Number,
    highPrice: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$small: 640px;
$productTitleColor: #2a2a2a;
$accentColor: #b30008;
$priceAccentColor: #866347;

.product-grid {
  &-item {
    margin: 10px;
    border-radius: 0.2em;
    padding: 1em;
    list-style:none;

    &-price{
        color:$priceAccentColor;
    }

    &-img{
        &:nth-child(1){
            z-index:2;
            position:relative;
            &:hover{
                opacity:0;
            }
        }
        &:nth-child(2){
            position: absolute;
            left: 0;
            z-index:1;

        }
    }

    &:hover{
        cursor:pointer;
        h1{
            opacity:.75;
            transition:all ease-out;
        }
    }

    a{
        position:relative;
        display:block;
        text-decoration:none;

        &:hover{
            h1{
                 text-decoration:underline;
            }
        }
    }

    h1 {
      font-size: 1rem;
      padding: 0 1em;
      color: $productTitleColor;
      letter-spacing:.03rem;
      line-height:1.5em;

        @media (min-width: $small) {
        font-size: .95rem;
        }
    }

    p{
        font-size:1rem;
        @media (min-width: $small) {
        font-size: .85rem;
        }
    }
    img{
        max-width:100%;
    }
    @media (min-width: $small) {
      width: 250px;
      font-size: 1.15rem;
    }
  }
}
</style>
