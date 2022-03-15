<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="text" v-model="email" placeholder="請輸入 Email">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" v-model="password.password" placeholder="請輸入密碼">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" v-model="password.confirm" placeholder="確認密碼">
    </div>
    <div class="wrapper__login-button" @click.prevent="submitForm">登入</div>
    <div class="wrapper__login-button">立即註冊</div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  position: absolute;
  top: 50%;
  right: 0;
  left: 0;
  transform: translateY(-50%);
  &__img {
    display: block;
    margin: 0 auto .4rem auto;
    width: .66rem;
    height: .66rem;
  }
  &__input {
    height: .48rem;
    margin: 0 .4rem .16rem .4rem;
    padding: 0 .16rem 0 .16rem;
    background: #F9F9F9;
    border: 1px solid rgba(0,0,0, 0.10);
    border-radius: 6px;
    border-radius: 6px;
    &__content {
      line-height: .48rem;
      border: none;
      outline: none;
      background: none;
      width: 100%;
      height: 100%;
      font-size: .16rem;
      &::placeholder {
        color: rgba(0,0,0, 0.05);
      }
    }
  }
  &__login-button {
    margin: .32rem .4rem 0 .4rem;
    line-height: .48rem;
    font-size: .16rem;
    text-align: center;
    background: #0091FF;
    box-shadow: 0 .04rem .08rem 0 rgba(0, 145, 255, 0.32);
    border-radius: .04rem;
    border-radius: .04rem;
    color: #fff;
  }
}
</style>

<script>
import useVuelidate from '@vuelidate/core'
import { required, email, minLength, sameAs } from '@vuelidate/validators'

export default {
  data () {
    return {
      v$: useVuelidate(),
      email: '',
      password: {
        password: '',
        confirm: ''
      }
    }
  },
  validations () {
    return {
      email: { required, email },
      password: {
        password: { required, minLength: minLength(6) },
        confirm: { required, sameAs: sameAs(this.password.password) }
      }
    }
  },
  methods: {
    submitForm () {
      this.v$.$validate()
      if (!this.v$.$error) {
        alert('Form successfully submitted.')
      } else {
        alert('Form failed submitted.')
      }
    }
  }
}
</script>
