<script>
export default {
  name:"Main"
}
</script>

<template>
  <Main>
    <section class="container">
      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/1.webp" alt="">
          <img class="second-img" src="../assets/img/1b.webp" alt="">
          <span class="discount">-50%</span>
          <span class="sustain">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Levi's</span>
          <h4>Related fit tee unisex</h4>
          <div class="price">
            <span class="new-price">14,99 &euro;</span>
            <span class="old-price">29,99 &euro;</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/2.webp" alt="">
          <img class="second-img" src="../assets/img/2b.webp" alt="">
          <span class="discount">-30%</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Guess</span>
          <h4>Roses tee</h4>
          <div class="price">
            <span class="new-price">20,99 &euro;</span>
            <span class="old-price">29,99 &euro;</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/3.webp" alt="">
          <img class="second-img" src="../assets/img/3b.webp" alt="">
          <span class="discount">-30%</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Come zucchero filato</span>
          <h4>Voglia di colori pastello</h4>
          <div class="price">
            <span class="new-price">129,99 &euro;</span>
            <span class="old-price">184,99 &euro;</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/4.webp" alt="">
          <img class="second-img" src="../assets/img/4b.webp" alt="">
          <span class="discount">-50%</span>
          <span class="sustain">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Levi's</span>
          <h4>Tee unisex</h4>
          <div class="price">
            <span class="new-price">14,99 &euro;</span>
            <span class="old-price">29,99 &euro;</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/5.webp" alt="">
          <img class="second-img" src="../assets/img/5b.webp" alt="">
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Maya Deluxe</span>
          <h4>Stripe bodice</h4>
          <div class="price">
            <span class="new-price">99,99 &euro;</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="image-box">
          <img class="first-img" src="../assets/img/6.webp" alt="">
          <img class="second-img" src="../assets/img/6b.webp" alt="">
          <span class="sustain-last">Sostenibilità</span>
          <span class="heart">&hearts;</span>
        </div>
        <div class="text-box">
          <span class="brand">Esprit</span>
          <h4>Maglione - black</h4>
          <div class="price">
            <span class="new-price">29,99 &euro;</span>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss">
@use "../scss/partials/colors" as *;

.container{
  margin: 100px auto;
  max-width: 1200px;
  height: fit-content;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;

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
      }
      .sustain{
        background-color: $sustain-bg;
        left: 40px;
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

      .text-box{
        position: relative;
        display: flex;
        flex-direction: column;
        font-size: 0.9em;

        .price, .brand{
          font-size: 0.8em;
        }

        .price{
          .new-price{
            color: $new-price;
          }
          .old-price{
            text-decoration: line-through;
          }
        }
      }
    }
  }
}

</style>