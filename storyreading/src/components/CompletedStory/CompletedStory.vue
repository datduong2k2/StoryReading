<template lang="pug">
  .right-aside
  .header
    h2 | TRUYỆN ĐÃ HOÀN THÀNH
    p.text XEM THÊM &gt;
  hr.horizontal-line
  // Repeat this block for each mobile-box item
  .mobile-box(v-for='item in items' :key='item.id')
    img(:src='item.cover' :alt='item.title')
    .box-description
      p
        strong {{ item.title }}
        br
        span(v-if='item.desc_short') {{ item.desc_short }}
        br
        span Tác giả: {{ item.author }}
        br
        span Chương hiện tại: {{ item.chapter }}
        br
        span Tất cả chương: {{ item.chapter_all }}
</template>

<script>
import cardlist01 from "../../assets/z_data/cardlist01.json"; // Adjust the path based on your project structure

export default {
  data() {
    return {
      items: cardlist01.cards.slice(0, 5), // Lấy 5 cuốn sách đầu tiên từ JSON
    };
  },
};
</script>

<style scoped <style lang="stylus">
.right-aside
  grid-area right-aside
  background-color #ffffff

.header
  display flex
  justify-content space-between
  align-items center
  background-color #ffffff
  h2
    margin 0
    font-size 12px

.text
  color #007bff
  cursor pointer
  font-size 12px

.horizontal-line2
  width 100%
  height 1px
  background-color #000
  margin-bottom 10px

.mobile-box
  height auto
  display flex
  align-items center
  padding 10px
  background-color #ffffff
  border-bottom 1px solid #ccc
  img
    width 80px
    height 100px
    object-fit cover
    border-radius 5px
    margin-right 10px

.box-description
  flex 1
  font-size 14px
  font-family "Times New Roman", Times, serif
  text-align justify

.horizontal-line
  border none
  border-top 1px solid #ccc
  margin-top 0
</style>
