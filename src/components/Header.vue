<script>
export default {
  name:"Header"
}
</script>

<template>
  <header>
    <section class="top-bar">
      <div class="top-menu">
        <ul class="category">
          <li>Donna</li>
          <li>Uomo</li>
          <li>Bambini</li>
        </ul>

        <img src="/public/boolean-logo.png" alt="logo">

        <ul class="icons">
          <li><i class="fa-regular fa-user"></i></li>
          <li><i class="fa-regular fa-heart"></i></li>
          <li><i class="fa-solid fa-bag-shopping"></i></li>
        </ul>
      </div>
    </section>
  </header>
</template>

<style lang="scss" scoped>
@use "../scss/partials/colors" as *;

.top-bar{
  background-color: $top-bar-bg;
  position: fixed;
  top: 0;
  width: 100%;
  box-shadow: 0 1px grey;
  display: flex;
  justify-content: center;
  z-index: 999;
  
  .top-menu{
    height: 70px;
    max-width: 1200px;
    width: 98%;
    color: $top-bottom-menu;
    display: flex;
    justify-content: space-between;
    align-items: center;

    ul {
      font-weight: bold;
      li{
        display: inline-block;
        list-style: none;
        padding: 5px 3px 0 0;
        margin: 0 5px;
        &:hover{
          text-decoration: underline;
          cursor: pointer;
        }
      }
    }
    img{
      height: 30px;
      width: 125px;
    }
  }
}

</style>