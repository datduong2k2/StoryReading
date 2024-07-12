<template lang="pug">
  .top-view-block
  // Header
  .header
    h2 | TRUYỆN XEM NHIỀU
    p.text XEM THÊM &gt;
  hr.horizontal-line
  // Options
  // Books
  .books
    .book-container
      .book(v-for='(book, index) in convertBooks' :key='index')
        img(:src='book.image' alt='Book Cover')
        p {{ book.name }}
</template>

<script>
export default {
  name: "NewBooksBlock",
  data() {
    return {
      convertBooks: [
        {
          image:
            "https://www.nae.vn/ttv/ttv/public/images/story/0ab9fbe917d20cac55123ea2a3267ed3c3d8ad4921f25612adcd782c1826ca73.jpg",
          name: "Truyện 1",
        },
        {
          image:
            "https://www.nae.vn/ttv/ttv/public/images/story/8b07c672dd146c782feca74cb80c210657a9354f72833f3021ee8b08598d0f5e.jpg",
          name: "Truyện 2",
        },
        {
          image:
            "https://www.nae.vn/ttv/ttv/public/images/story/82d6ce1bf3b8a1947e62d15d3c9a7c7eeee13edbdbd54cc7cdc3191685518b59.jpg",
          name: "Truyện 3",
        },
        {
          image:
            "https://www.nae.vn/ttv/ttv/public/images/story/17b5efa8081ec08b62dc6372b6a130756409fa1b99e5908225c7b4a7902284de.jpg",
          name: "Truyện 4",
        },
      ],
    };
  },
};
</script>

<style scoped <style lang="stylus">
.top-view-block
  font-weight bold
  font-size 18px
  background-color #ffffff

.header
  display flex
  justify-content space-between
  align-items center
  h2
    margin 0
    font-size 12px

.text
  color #007bff
  cursor pointer
  font-size 12px

.books
  display flex
  flex-wrap wrap

.book-container
  width 100%
  display flex
  flex-wrap wrap

.book
  width calc(25% - 5px)
  margin-bottom 10px
  text-align center
  color black
  cursor none
  text-decoration none
  margin-left 5px
  img
    width 100%
    aspect-ratio 0.8
    border-radius 5px
    object-fit cover
  p
    margin-top 10px
    font-weight bold

.horizontal-line
  border none
  border-top 1px solid #ccc
  margin-top 0
</style>
