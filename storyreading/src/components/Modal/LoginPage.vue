<template lang="pug">
form.login__tab.px-6.py-2.flex.flex-col.gap-5
    div.login__tab__email.inline-flex.items-center.text-base.text-center.border.px-4
        i.pi.pi-user
        input.outline-none.login__tab-email.py-2.px-3(type="email" placeholder="Tài khoản" v-model="username")
    div.login__tab__password.inline-flex.items-center.text-base.text-center.border.px-4
        i.pi.pi-key
        input.outline-none.login__tab-password.py-2.px-3(type="password" placeholder="Mật khẩu" v-model="password")
    div.login__tab__forgot.text-right.text-sky-500
        a(href="#") Quên mật khẩu ?
    div.login__tab__btn.text-base.rounded-sm.text-center.py-2
        button(type="submit") Đăng nhập    
    div.login__tab__login.text-base.text-sky-800.py-2.px-3.flex.items-center.justify-center.gap-2
        i.pi.pi-facebook 
        a(href="#") Đăng nhập bằng Facebook  
</template>

<script>
export default {
  components: {},
  data() {
    return {
      username: "",
      passsword: "",
    };
  },
};
</script>

<style lang="stylus">
.login__tab
    padding 22px 30px
    .login__tab__btn
        background #BF2C24
        color white
        cursor pointer
        transition all 0.5s
        &:hover
            background #ed4259
    input
        width 100%
.login__tab__login
    transition all 0.5s
    &:hover
        background #c5d9f2
</style>
