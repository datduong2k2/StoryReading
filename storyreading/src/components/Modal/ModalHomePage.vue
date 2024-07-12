<template lang="pug">
div.modal__container.bg-white.text-black.rounded-md.p-6(@click="closeModal")
    div.modal__inner
        slot
        button.modal-close.btn.px-3.py-5(@click = 'ToggleModal') 
            i.pi.pi-times
</template>

<script>
export default {
  props: ["ToggleModal"],
  methods: {
    closeModal(event) {
      if (event.target.classList.contains("modal__container")) {
        this.ToggleModal();
      }
    },
  },
};
</script>
<style lang="stylus" scoped>
@media screen and (max-width: 778px)
  .modal__container
      position fixed
      top 0
      left 0
      right 0
      bottom 0
      z-index 99
      background-color rgba(0, 0, 0, 0.2)
      display flex
      align-items center
      justify-content center
      .modal__inner
          position relative
          background #fff
          width 80%
          height 500px
          padding 22px 32px
          button.modal-close
              position absolute
              top 10px
              right 10px

@media screen and (min-width: 778px)
  .modal__container
      position fixed
      top 0
      left 0
      right 0
      bottom 0
      z-index 99
      background-color rgba(0, 0, 0, 0.2)
      display flex
      align-items center
      justify-content center
      .modal__inner
          position relative
          background #fff
          width 50%
          height 500px
          padding 22px 32px
          button.modal-close
              position absolute
              top 10px
              right 10px
</style>
