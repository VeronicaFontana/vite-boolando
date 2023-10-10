<script>
export default {
  name:"Footer"
}
</script>

<template>
  <footer>
    <section class="bottom-bar">
      <div class="bottom-menu">
        <div class="legal-info">
          <span>Boolando s.r.l</span>
          <ul>
            <li>Informazioni legali</li>
            <li>Informativa sulla privacy</li>
            <li>Diritto di recesso</li>
          </ul>
        </div>
        <div class="social">
          <span>Trovaci anche su</span>
          <ul>
            <li><i class="fa-brands fa-square-twitter"></i></li>
            <li><i class="fa-brands fa-square-facebook"></i></li>
            <li><i class="fa-brands fa-square-instagram"></i></li>
            <li><i class="fa-brands fa-square-pinterest"></i></li>
            <li><i class="fa-brands fa-square-youtube"></i></li>
          </ul>
        </div>
      </div>
    </section>
  </footer>
</template>

<style lang="scss" scoped>
@use "../scss/partials/colors" as *;
@use "../scss/partials/general" as *;

.bottom-bar{
  background-color: $bottom-bar-bg;
  display: flex;
  justify-content: center;
  .bottom-menu{
    height: 70px;
    max-width: 1200px;
    width: 98%;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .legal-info{
      span{
        font-weight: bold;
      }
      ul{
        font-size: 0.8em;
        li{
          display: inline-block;
          list-style: none;
          padding: 5px 3px 0 0;
        }
      }
    }
    .social{
      span{
        font-size: 0.7em;
      }
      ul{
        font-size: 0.8em;
        li{
          display: inline-block;
          list-style: none;
          padding: 5px 3px 0 0;

          i{
            color: white ;
          }
        }
      }
    }
  }
  
}

</style>