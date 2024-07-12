<template lang="pug">
  .slideshow
    .slide(v-for='(image, index) in images' :key='index' :class='{ active: index === currentIndex }')
      img(:src='image. src' :alt="'Slideshow Image ' + (index + 1)")
    // Thanh điều hướng (pagination)
    .pagination
      span.dot(v-for='(image, index) in images' :key='index' :class='{ active: index === currentIndex }' @click='goToSlide(index)')
    // Biểu tượng chuyển slide
    .controls
      span.prev(@click='prevSlide') &#x276E;
      span.next(@click='nextSlide') &#x276F;
</template>

<script>
export default {
  name: "SlideShow",
  data() {
    return {
      currentIndex: 0,
      intervalId: null,
      images: [
        { src: "https://truyen.tangthuvien.vn/images/slide8.jpg" },
        { src: "https://truyen.tangthuvien.vn/images/slide7.jpg" },
        { src: "https://truyen.tangthuvien.vn/images/slide9.jpg" },
      ],
    };
  },
  mounted() {
    this.startSlideshow();
  },
  methods: {
    startSlideshow() {
      this.intervalId = setInterval(() => {
        this.nextSlide();
      }, 3000); // Thay đổi slide mỗi 3 giây (3000 milliseconds)
    },
    stopSlideshow() {
      clearInterval(this.intervalId);
    },
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
    prevSlide() {
      this.currentIndex =
        this.currentIndex === 0
          ? this.images.length - 1
          : this.currentIndex - 1;
    },
    goToSlide(index) {
      this.currentIndex = index;
    },
  },
  beforeUnmount() {
    this.stopSlideshow();
  },
};
</script>

<style scoped <style lang="stylus">

.slideshow
	margin-top 10px
	overflow hidden
	position relative
	margin-bottom 10px
	.slide
		display none
		top 0
		left 0
		width 100%
		height 100%
		&.active
			display block
		img
			width 100%
			height 100%
.pagination
	text-align center
	margin-top 10px
	.dot
		display inline-block
		width 10px
		height 10px
		background-color #bbb
		border-radius 50%
		margin 0 5px
		cursor pointer
		&.active
			background-color #555
.controls
	position absolute
	top 50%
	transform translateY(-50%)
	width 100%
	display flex
	justify-content space-between
	font-size 24px
	color #fff
	cursor pointer
	z-index 1
	margin-bottom 10px
	.prev
		left 20px
	.next
		right 20px
.controls .prev,
.controls .next
	user-select none
</style>
