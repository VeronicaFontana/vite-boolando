<script>
import prodotti from "../data/Products";
import Card from "./partials/Card.vue";

export default {
  name:"Main",

  data(){
    return{
      prodotti
    }
  },

  components:{
    Card
  }
}
</script>

<template>
  <main>
    <section class="container">
      <Card v-for="(prodotto, index) in prodotti" :key="index" :productObj="prodotto" />
    </section>
  </main>
</template>


<style lang="scss" scoped>
@use "../scss/partials/colors" as *;

.container{
  margin: 100px auto;
  max-width: 1200px;
  height: fit-content;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}

</style>