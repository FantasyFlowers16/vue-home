<template>
  <div class="news-item">

    <div class="news-item__title">{{data.newsTitle}}</div>
    <div class="news-item__text">{{data.newsText}}</div>

  </div>

</template>

<script>
export default {
  props: ['data'],
}

</script>

<style lang="sass" >

.news-item
  cursor: pointer
  background: #c9d6d8
  z-index: 10
  padding: 5px 10px
  border-radius: 10px
  border: 1px solid cadetblue
  opacity: 0.9
  text-align: left
  transition: all .2s ease-in
  max-height: 195px
  overflow: hidden
  line-height: 28px
  &:hover
    opacity: 1
    background-color: #cde4ea

  &__title
    margin: 20px 0 5px 0
    font-size: 24px
    font-weight: bold
  &__text
    font-size: 18px
    text-overflow: ellipsis
    max-height: 163px
    overflow: hidden
    display: -webkit-box
    -moz-line-clamp: 3
    -webkit-line-clamp: 3
    -webkit-box-orient: vertical
@media screen and (min-width: 768px)
  .news-item
    max-height: 195px
    overflow: hidden
    line-height: 28px
</style>