<template lang="pug">
  .right-aside
  .header
    h2 | TRUYỆN ĐỀ CỬ
    p.text XEM THÊM &gt;
  hr.horizontal-line
  // Repeat this block for each mobile-box item
  .mobile-box(v-for='item in items' :key='item.id')
    img(:src='item.imageUrl' :alt='item.alt')
    .box-description
      p
        | {{ item.title }} 
        br
        |           Th&#x1EC3; lo&#x1EA1;i: {{ item.genre }} 
        br
        |           T&aacute;c gi&#x1EA3;: {{ item.author }} 
        br
        |           L&#x1B0;&#x1EE3;t xem: {{ item.views }} 
        br
        |           T&igrave;nh tr&#x1EA1;ng: {{ item.status }} 
        br
        |           S&#x1ED1; ch&#x1B0;&#x1A1;ng: {{ item.chapters }}

</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          imageUrl:
            "https://www.nae.vn/ttv/ttv/public/images/story/0ab9fbe917d20cac55123ea2a3267ed3c3d8ad4921f25612adcd782c1826ca73.jpg",
          alt: "Image 1",
          title: "Luân hồi lạc viên",
          genre: "Đồng nhân",
          author: "Na nhất chích vân tử",
          views: "847948489",
          status: "chưa hoàn thành",
          chapters: "899",
        },
        {
          id: 2,
          imageUrl:
            "https://www.nae.vn/ttv/ttv/public/images/story/0ab9fbe917d20cac55123ea2a3267ed3c3d8ad4921f25612adcd782c1826ca73.jpg",
          alt: "Image 1",
          title: "Luân hồi lạc viên",
          genre: "Đồng nhân",
          author: "Na nhất chích vân tử",
          views: "847948489",
          status: "chưa hoàn thành",
          chapters: "899",
        },
        // Add more items as needed
      ],
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

.section-header
  display flex
  justify-content space-between
  align-items center
  background-color #ffffff
  h5
    height 20px
  a
    color #333
    text-decoration none

.horizontal-line2
  width 100%
  height 1px
  background-color #000
  margin-bottom 10px

.mobile-box
  height 100px
  display flex
  align-items center
  padding 10px
  background-color #ffffff
  img
    width 70px
    aspect-ratio 0.7
    border-radius 5px
    margin-right 10px

.box-description
  flex 1
  font-size 14px
  font-family "Times New Roman", Times, serif
  text-align left

.horizontal-line
  border none
  border-top 1px solid #ccc
  margin-top 0
</style>
