<template lang="pug">
.footer
  img.logo(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnRyNjTC0YyGo6zBrXw9m7FABlPEjhM14NiQ&s' alt='Logo')
  p
    |  © 2007 Tàng Thư Viện - Chính sách
    br
    |       Tàng Thư Viện là sân chơi mở và free cho cộng đồng fan kiếm hiệp, tiên hiệp, ngôn tình. Chúc các bạn có những giây phút thư giãn thoải mái sau giờ làm việc và học tập căng thẳng.

</template>

<script>
export default {
  name: "FooterPage",
};
</script>

<style scoped <style lang="stylus">
.footer
  background-color #eeeeee
  color #000000
  text-align center
  padding 8px
  bottom 0
  margin-top 10px
  display flex
  align-items center
  p
    float left
    position relative
    min-height 1px
    padding-right 15px
    padding-left 15px
    box-sizing border-box
    font-size 12px
    font-family "Roboto", sans-serif
    line-height 1.5
    color #333

.logo
  display none

@media (min-width: 678px)
  .footer
    text-align left
    p
      font-size 13px
      margin-right 50px
  .logo
    display flex !important
    height 60px
    margin-right 80px
    margin-left 20px
</style>
