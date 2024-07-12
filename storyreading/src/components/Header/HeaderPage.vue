<template lang="pug">
header
    .logoContainer.flex.justify-between.items-end 
        .logo__image 
            router-link(to="#")
        .searchContainer 
            Search
        AccountButton 
    
    .menuContainer 
        Menu 


</template>
<script>
import Search from "./SearchHeader.vue";
import AccountButton from "./AccountButton.vue";
import Menu from "./MenuHeader.vue";
export default {
  components: {
    Search,
    AccountButton,
    Menu,
  },
};
</script>
<style scoped lang="stylus">
// < 600px
@media screen and (max-width: 600px)
    .logoContainer
        width 90%
        background white
        height 75px
        padding 0 5px
        margin 0 auto
        margin-bottom 50px
        flex-direction column
        justify-content center
        align-items center
        padding 15px

        .logo__image
            display none
            width 100px
            height 52px
            background url("https://truyen.tangthuvien.vn/images/logo-web.png")
            background-size cover

        .searchContainer
            margin-top 50px
            margin-bottom 20px
            margin-right 0px
            width 80%

    .menuContainer
        background #2798a1
        height 40px
        padding 0px

// 600px - 768px
@media screen and (min-width: 600px)
    .logoContainer
        width 100%
        background white
        height 75px
        padding 0 5px
        margin-bottom 5px

        .logo__image
            display none
            width 100px
            height 52px
            background url("https://truyen.tangthuvien.vn/images/logo-web.png")
            background-size cover

        .searchContainer
            margin-right 50px

    .menuContainer
        background #2798a1
        height 40px
        padding 0px

// 768px - 992px
@media screen and (min-width: 768px)
    .logoContainer
        width 100%
        background white
        height 75px
        padding 0 70px
        margin-bottom 5px

        .logo__image
            display none
            width 100px
            height 52px
            background url("https://truyen.tangthuvien.vn/images/logo-web.png")
            background-size cover

        .searchContainer
            margin-right 50px

    .menuContainer
        background #2798a1
        height 40px
        padding 0 10px



// 992px - 1200px
@media screen and (min-width: 992px)
    .logoContainer
        width 100%
        background white
        height 75px
        margin-bottom 12px
        padding 0 70px

        .logo__image
            display block
            width 220px
            height 52px
            background url("https://truyen.tangthuvien.vn/images/logo-web.png")
            background-size cover
            margin-left 50px

        .searchContainer
            margin-right 50px

    .menuContainer
        background #2798a1
        height 40px
        padding 0 100px


// > 1200px
@media screen and (min-width: 1200px)
    .logoContainer
        width 100%
        background white
        height 85px
        margin-bottom 15px
        padding 0 100px

        .logo__image
            width 220px
            height 52px
            background url("https://truyen.tangthuvien.vn/images/logo-web.png")
            background-size cover
            margin-left 50px

        .searchContainer
            margin-right 50px

    .menuContainer
        background #2798a1
        height 40px
        padding 0 100px
</style>
