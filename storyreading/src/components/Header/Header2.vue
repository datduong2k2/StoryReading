<template lang="pug">
	.header
		.logo
			img(src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnRyNjTC0YyGo6zBrXw9m7FABlPEjhM14NiQ&s' alt='logo')
		.search-bar
			input(type='text' placeholder='Search...')
		.account Account
		.account2
			img(src='https://banner2.cleanpng.com/20180516/zq/kisspng-computer-icons-google-account-icon-design-login-5afc02dab4a218.0950785215264652427399.jpg' alt='login')
	</template>

<script>
export default {
  name: "HeaderPage",
};
</script>

<style lang="stylus">
 .header
  margin-top 20px
  grid-area header
  background-color #ffffff
  display flex
  justify-content space-around
  align-items center
  .logo
    img
      height 60px
      width auto

.logo
  margin left 10px
  justify-content flex-start

.search-bar
  flex 2
  text-align center
  input
    width 100%
    max-width 300px
    height 25px
    padding 8px
    font-size 18px
    border-radius 10px
    border 1px solid #ccc

.account
  text-align right
  position relative
  border 1px solid #ccc
  border-radius 10px
  padding 10px
  &::after
    margin-left 10px

@media (min-width: 678px)
  .account2
    display none

@media (max-width: 678px)
  .header
    .search-bar
      display none
    .logo
      img
        height 30px
        width auto
  .account
    display none
  .account2
    display flex
    justify-content flex-end
    align-items center
    flex 1
    img
      display flex
      justify-content flex-end
      height 30px
      width 30px
      display flex
      justify-content flex-end
</style>
