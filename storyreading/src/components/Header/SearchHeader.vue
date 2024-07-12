<template lang="pug">
form.flex(action="#")
    input.search__box.border.outline-none(type="text" placeholder="Nhập tên truyện hoặc tác giả")
    p.search__button.text-center.flex.items-center
        button(type="submit") ⌕
</template>

<style scoped lang="stylus">

form
    height 45px
    .search__box
        width 350px
        padding 0 15px

.search__button
    width 40px
    background #2798a1

    button
        color white
        font-size 20px
        font-weight 700
        width 100%
</style>
