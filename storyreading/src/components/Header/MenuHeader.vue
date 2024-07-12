<template lang="pug">
.menu-nav
    div.buttonDown.hidden
        a(href="#")
            i.pi.pi-download
    ul.flex.items-center.w-full.text-sm 
        li.selected.items-center.gap-2.content-center
                i.pi.pi-bars  
                p Thể loại
        li.item.items-center.justify-center 
            router-link(to="#") Diễn đàn  
        li.item.items-center.justify-center 
            a(href="#rank") Bảng xếp hạng
        li.item.items-center.justify-center 
            router-link(to="#") Bộ lọc
        li.item.items-center.justify-center     
            router-link(to="#") Reviews
        li.item.items-center.justify-center
            router-link(to="#") Cửa hàng
        li.download.gap-2.items-center
            .download__icon 
                i.pi.pi-mobile 
            .download__text 
                router-link(to="#") Tải App
    ul
</template>

<script></script>

<style scoped lang="stylus">
@media screen and (max-width: 600px)
    .menu-nav
            color white
            font-weight 450
            font-size 15px
            width 100%
            height 100%
            display flex
            align-items center
            flex-wrap wrap
            position relative

            .buttonDown
                cursor pointer
                position fixed
                top 10%
                right 0
                padding 25px
                border-radius 50%
                background #2798a1
                height 50px
                width 50px
                text-align center
                display flex
                align-items center
                justify-content center
                color white
            ul
                height 100%
                justify-content space-around

                li
                    height 100%
                    cursor pointer
                    float left
                    display flex
                    align-items center
                    padding 0 5px
                    transition all 0.3s
                    font-size 12px
                    router-link
                        height 25px
                        text-align center


            .download
                    display none
                    margin-left 30px
                    &:hover
                            color #ffeea8
                .item
                    transition all 0.3s
                    &:hover
                        background #077C86

                .selected
                        width 270px
                        margin-left 10px
                        background #077C86
                        margin-right 40px
                        display none
// 600px - 768px
@media screen and (min-width: 600px)
    .menu-nav
        color white
        font-weight 450
        font-size 15px
        width 100%
        height 100%
        display flex
        align-items center

            i
                font-size 32px
                background #2798a1
                padding 7px
                border-radius 50%
        ul
            height 100%
            justify-content space-around
            li
                height 100%
                cursor pointer
                float left
                display flex
                align-items center
                padding 0 10px
                transition all 0.3s
                router-link
                    height 25px
                    text-align center

        .download
                margin-left 30px
                &:hover
                        color #ffeea8
            .item
                transition all 0.3s
                &:hover
                    background #077C86

            .selected
                    width 270px
                    margin-left 10px
                    background #077C86
                    margin-right 40px
                    display none


// 768px - 992px
@media screen and (min-width: 768px)
    .menu-nav
        color white
        font-weight 450
        font-size 15px
        width 100%
        height 100%
        .buttonNav
            display none
        ul
            height 100%
            justify-content center
            li
                height 100%
                cursor pointer
                float left
                display flex
                align-items center
                padding 0 10px
                transition all 0.3s
                router-link
                    height 25px
                    text-align center

        .download
                margin-left 30px
                &:hover
                        color #ffeea8
            .item
                transition all 0.3s
                &:hover
                    background #077C86

            .selected
                    width 270px
                    margin-left 10px
                    background #077C86
                    margin-right 40px
                    display flex
// 992px - 1200px
@media screen and (min-width: 992px)
    .menu-nav
        color white
        font-weight 450
        font-size 15px
        width 100%
        height 100%
        ul
            height 100%

            li
                height 100%
                cursor pointer
                float left
                display flex
                align-items center
                padding 0 10px
                transition all 0.3s
                router-link
                    height 25px
                    text-align center

        .download
                margin-left 30px
                &:hover
                        color #ffeea8
            .item
                transition all 0.3s
                &:hover
                    background #077C86

            .selected
                    width 220px
                    margin-left 30px
                    background #077C86
                    margin-right 30px
// > 1200px
@media screen and (min-width: 1200px)
    .menu-nav
        color white
        font-weight 450
        font-size 15px
        width 100%
        height 100%
        ul
            height 100%

            li
                height 100%
                cursor pointer
                float left
                display flex
                align-items center
                padding 0 20px
                transition all 0.3s
                router-link
                    height 25px
                    text-align center

        .download
                margin-left 50px
                &:hover
                        color #ffeea8
            .item
                transition all 0.3s
                &:hover
                    background #077C86

            .selected
                    width 270px
                    margin-left 50px
                    background #077C86
                    margin-right 40px
</style>
