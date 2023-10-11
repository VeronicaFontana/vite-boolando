<script>
export default {
  name: "Card",

  props:{
    productObj: Object
  },

  computed:{
    newPrice(){
      return this.productObj.fullPrice.toFixed(2, '0')
    },
    oldPrice(){
      return this.productObj.lastPrice.toFixed(2, '0')
    }
  }
}
</script>

<template>
  <div class="card">
        <div class="image-box">
          <img class="first-img" :src="`/img/${productObj.primaryImage}`" alt="">
          <img class="second-img" :src="`/img/${productObj.secondaryImage}`" alt="">
          <span v-if="productObj.discount != null" class="discount">{{ productObj.discount }}</span>
          <span v-if="productObj.sostenibilita" class="sustain">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">{{ productObj.marca }}</span>
          <h4>{{ productObj.modello }}</h4>
          <div class="price">
            <span v-if="productObj.fullPrice != null" class="new-price">{{ newPrice }} &euro;</span>
            <span :class="{'old-price': productObj.fullPrice != null}">{{ oldPrice }} &euro;</span>
          </div>
        </div>
      </div>
</template>

<style lang="scss" scoped>
@use "../../scss/partials/colors" as *;

.card{
    position: relative;
    width: 30%;
    min-width: calc(1200px / 6);
    height: 40%;
    margin-bottom: 30px;

    .image-box{
      img{
        max-width: 100%;
        max-height: 100%;
      }
      .first-img{
        position: absolute;
        top: 0;
        left: 0;

        &:hover{
          opacity: 0;
        }
      }
      .discount{
        background-color: $discount-bg;
        left: 0;
        color: white;
        position: absolute;
        padding: 5px;
        bottom: 70px;
        font-size: 0.7em;
      }
      .sustain{
        background-color: $sustain-bg;
        left: 40px;
        color: white;
        position: absolute;
        padding: 5px;
        bottom: 70px;
        font-size: 0.7em;
      }
      .heart{
        background-color: white;
        padding: 5px 15px;
        font-size: 2em;
        position: absolute;
        top: 5px;
        right: 0;

        &:hover{
          color: $heart-hover;
          cursor: pointer;
        }
      }
    }
    .text-box{
      position: relative;
      display: flex;
      flex-direction: column;
      font-size: 0.9em;
      padding-top: 5px;

      .brand{
        font-size: 1em;
        font-weight: bold;
      }

      .price{
        font-size: 0.8em;
        .new-price{
          color: $new-price;
          margin-right: 8px;
        }
        .old-price{
          text-decoration: line-through;
        }
      }
    }
  }

</style>