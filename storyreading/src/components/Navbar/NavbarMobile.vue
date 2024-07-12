<template lang="pug">
 .mobile-navbar
  a(href='#')
    img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMzigP1lbSxHKc43srls1iwvp_ZQQorHj9VA&s')
    |       Thể loại
  a(href='#')
    img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMzigP1lbSxHKc43srls1iwvp_ZQQorHj9VA&s')
    |       Xếp hạng
  a(href='#')
    img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMzigP1lbSxHKc43srls1iwvp_ZQQorHj9VA&s')
    |       Bộ lọc
  a(href='#')
    img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMzigP1lbSxHKc43srls1iwvp_ZQQorHj9VA&s')
    |       Top User
  a(href='#')
    img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMzigP1lbSxHKc43srls1iwvp_ZQQorHj9VA&s')
    |       Review
  // Other mobile nav links

</template>

<script>
export default {
  name: "MobileNavbar",
};
</script>

<style scoped <style lang="stylus">
.mobile-navbar
  flex-grow 1
  display flex
  justify-content space-around
  grid-area mobile-navbar
  background-color #ffffff
  height auto
  margin-bottom 20px
  a
    display flex
    flex-direction column
    align-items center
    text-decoration none
    color #333
    font-size 12px
  img
    width 70%
    aspect-ratio 1
    margin-bottom 5px
@media (min-width: 678px)
    .mobile-navbar
      display none
</style>
