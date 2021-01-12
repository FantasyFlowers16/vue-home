<template>
  <router-link to="/" class="back" >Назад</router-link>
  <h1>Photo:</h1>
  <div v-for="item in this.photoList" :key="item.id">
    <photo-item ></photo-item>
  </div>

</template>

<script>
import PhotoItem from "@/components/itemPhoto";


export default {
  components: {
    PhotoItem
  },
  name: "photo-page",
  photoList:[
      {
        url:"https://is.gd/xNetps",
        id:1
      },
      {
        url:"https://is.gd/dlduXc",
        id:2
      },
      {
        url:"https://is.gd/6ISirt",
        id:3
      },
      {
        url:"https://is.gd/iEPxwm",
        id:4
      },{
        url:"https://is.gd/v8WtTv",
        id:5
      },{
        url:"https://is.gd/y87P2w",
        id:6
      },{
        url:"https://is.gd/NjTZsr",
        id:7
      },{
        url:"https://is.gd/Rx7SPg",
        id:8
      }




  ],
}
</script>

<style lang="sass">
.back
  text-decoration: none
  color: black
  text-align: left
  padding-top: 20px
  padding-left: 40px
  position: relative
  cursor: pointer
  display: block
  &:before
    content: ''
    display: block
    position: absolute
    background-image: url('../assets/arrow.png')
    background-size: cover
    width: 16px
    height: 12px
    left: 10px

</style>