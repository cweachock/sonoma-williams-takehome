<template>
<h2>{{textHeader}}</h2>
</template>

<script>

export default {
  name: 'textBlock',
  props: {
    textHeader: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h2{
    text-align:center;
}
</style>
