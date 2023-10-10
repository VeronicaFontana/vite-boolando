<script>
export default {
  name:"Footer"
}
</script>

<template>
  <Footer>
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
  </Footer>
</template>

<style lang="scss">
@use "../scss/partials/colors" as *;

.bottom-bar{
  background-color: $bottom-bar-bg;
  display: flex;
  justify-content: center;

  .legal-info{
    span{
      font-weight: bold;
    }
    ul{
      font-size: 0.8em;
    }
  }
  .social{
    span{
      font-size: 0.7em;
    }
  }
}

</style>