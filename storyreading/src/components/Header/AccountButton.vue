<template lang="pug">
button.accountContainer.flex.gap-1.border.py-2.px-4.items-center(@click="() => ToggleModal('buttonTrigger')")
    .account__icon
        i.pi.pi-address-book
    .account 
        i Tài khoản
Modal(v-if="modalTriggers.buttonTrigger" :ToggleModal="() => ToggleModal('buttonTrigger') ")
    .account__tab.flex.items-center.justify-around.text-2xl.my-2
        button.account__tab-login.px-6.py-2(:class="{active: StateButton.Login}",@click="() => switchTab('login')")
            p.account__tab-title Đăng nhập
        button.account__tab-signup.px-6.py-2(:class="{active: StateButton.Signup}",@click="() => switchTab('signup')")
            p.account__tab-title Đăng ký
    Login(v-if="StateButton.Login")     
    Signup(v-if="StateButton.Signup")   
</template>

<script>
import { ref } from "vue";
import Modal from "../Modal/ModalHomePage.vue";
import Login from "../Modal/LoginPage.vue";
import Signup from "../Modal/SignupPage.vue";

export default {
  components: {
    Modal,
    Login,
    Signup,
  },
  data() {
    return {};
  },
  setup() {
    const StateButton = ref({
      Login: true,
      Signup: false,
    });
    const switchTab = (state) => {
      switch (state) {
        case "login": {
          StateButton.value["Login"] = true;
          StateButton.value["Signup"] = false;

          break;
        }
        case "signup": {
          StateButton.value["Login"] = false;
          StateButton.value["Signup"] = true;
          break;
        }
        default: {
          return;
        }
      }
    };
    const modalTriggers = ref({
      buttonTrigger: false,
    });
    const ToggleModal = (trigger) => {
      modalTriggers.value[trigger] = !modalTriggers.value[trigger];
    };
    return {
      modalTriggers,
      ToggleModal,
      StateButton,
      switchTab,
    };
  },
};
</script>

<style scoped lang="stylus">
@media screen and (max-width: 600px)
  .accountContainer
      font-size 16px
      color black
      font-weight 400
      transition all 0.3s

      &:hover
          background #ed4259
          color white
  .account__tab
      .active
          border-bottom 2px solid #BF2C24
      .not-active
          color #666
  .account
      i
        display none
  .account__tab
      font-size 16px
@media screen and (min-width: 600px)
  .accountContainer
      font-size 16px
      color black
      font-weight 400
      transition all 0.3s

      &:hover
          background #ed4259
          color white
  .account__tab
      .active
          border-bottom 2px solid #BF2C24
      .not-active
          color #666
</style>
