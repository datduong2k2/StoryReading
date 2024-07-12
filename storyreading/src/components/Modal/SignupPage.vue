<template lang="pug">
    form.login__tab.px-6.py-2.flex.flex-col.gap-5
        div.login__tab__email.inline-flex.items-center.text-base.text-center.border.px-4
            i.pi.pi-user
            input.outline-none.login__tab-email.py-2.px-3(type="email" placeholder="Tài khoản" v-model="username")
        div.login__tab__email.inline-flex.items-center.text-base.text-center.border.px-4
            i.pi.pi-envelope
            input.outline-none.login__tab-email.py-2.px-3(type="email" placeholder="Email" v-model="email")
        div.login__tab__password.inline-flex.items-center.text-base.text-center.border.px-4
            i.pi.pi-key
            input.outline-none.login__tab-password.py-2.px-3(type="password" placeholder="Mật khẩu" v-model="password")
        div.login__tab__password.inline-flex.items-center.text-base.text-center.border.px-4
            i.pi.pi-key
            input.outline-none.login__tab-password.py-2.px-3(type="password" placeholder="Nhập lại Mật khẩu" v-model="repassword")    
        
        div.login__tab__btn.text-base.rounded-sm.text-center.py-2
            button(type="submit") Đăng ký    
        div.login__tab__login.text-base.text-sky-800.py-2.px-3.flex.items-center.justify-center.gap-2
            i.pi.pi-facebook 
            a(href="#") Đăng ký bằng Facebook  
    </template>

<script>
export default {
  data() {
    return {
      email: "",
      username: "",
      password: "",
      repassword: "",
    };
  },
};
</script>

<style lang="stylus"></style>
