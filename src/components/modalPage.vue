<template>
  <transition name="modal-fade">
    <div class="modal-backdrop">
      <div class="modal">
        <header class="modal-header">
          <slot name="header">
          {{news.newsTitle}}

            <button
              type="button"
              class="btn-close"
              @click="close"
          >
            x
            </button>
          </slot>
        </header>
        <section class="modal-body">
          <slot name="body">
            {{news.newsText}}
          </slot>
        </section>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "ModalPage",
  methods: {
    close() {
      this.$emit('close');
    },
  },
  props:['news']
}
</script>

<style lang="sass"  scoped>
.modal-backdrop
  z-index: 11
  position: fixed
  top: 0
  bottom: 0
  left: 0
  right: 0
  background-color: rgba(0, 0, 0, 0.3)
  display: flex
  justify-content: center
  align-items: center


.modal
  width: 70%
  height: 50%
  background: #FFFFFF
  box-shadow: 2px 2px 20px 1px
  overflow-x: auto
  display: flex
  flex-direction: column
  border-radius:  20px


.modal-header
  padding: 15px
  display: flex
  font-size: 20px
  font-weight: bold


.modal-header
  border-bottom: 1px solid #eeeeee
  color: #4AAE9B
  justify-content: space-between

.modal-fade-enter,
.modal-fade-leave-active
  opacity: 0

.modal-fade-enter-active,
.modal-fade-leave-active
  transition: opacity .5s ease

.modal-body
  position: relative
  padding: 20px 15px
  text-align: left
  font-size: 18px
  line-height: 28px


.btn-close
  border: none
  font-size: 20px
  cursor: pointer
  font-weight: bold
  color: #4AAE9B
  background: transparent
  display: flex
  align-items: flex-start
  margin-left: 25px


.btn-green
  color: white
  background: #4AAE9B
  border: 1px solid #4AAE9B
  border-radius: 2px


</style>