<template>
  <div>
    <div class="menu">
      <div class="main-background"></div>

      <div class="menu__item-container">
        <transition><router-link to="/news"  class="menu__item">Новости</router-link></transition>
        <router-link to="/photo" class="menu__item">Фото дома</router-link>
      </div>
      <div class="menu__item-container">
        <router-link to="/chat" class="menu__item">Чат дома</router-link>
        <router-link to="/room" class="menu__item"> Квартиры в продаже</router-link>
      </div>
      <div class="menu__item-container">
        <a class="menu__item big">что-то большое</a>
      </div>

    </div>
</div>

</template>

<script>

export default {
  name: 'Home',
}
</script>

<style lang="sass">

.profile
  padding-top: 20px
  z-index: 10
  display: flex
  align-items: center
  &__photo
    width: 40px
    height: 40px
    border-radius: 40px
    background-image: url('../assets/avatar.jpg')
    padding: 10px
    background-size: cover
    background-position: 50% 70%
    background-color: white
  &__name
    margin: 20px
    color: #d3d8e0
    font-weight: bold
.main-background
  opacity: 0.85
  background-size: cover
  background: url('../assets/news.jpg') no-repeat 55% 20%
  min-width: 320px

  width: 100%
  position: absolute
  height: 100%
  margin-left: -10px
  margin-top: -10px


  //opacity: 0.7

  //z-index: 1
.menu
  display: flex
  flex-wrap: wrap

  &__item-container
    width: 100%
    display: flex
  &__item
    text-align: center
    text-decoration: none
    background: #dedcdc
    opacity: 0.85
    width: 100%
    color: black
    display: flex
    align-items: center
    justify-content: center
    min-height: 80px
    border-radius: 10px
    margin-top: 10px
    padding: 20px
    box-shadow: 3px 4px 4px rgba(1, 0, 44, 0.55)
    cursor: pointer
    font-weight: bold
    transition: all .2s ease-in
    &:nth-child(2n)
      margin-left: 10px
    &:hover
      background: white
      font-size: 17px
@media screen and (min-width: 768px)
  .profile
    padding: 20px
  .menu
    &__item-container
      justify-content: space-around
      padding: 0 20px
    &__item
      &.big
        max-width: 100%



</style>