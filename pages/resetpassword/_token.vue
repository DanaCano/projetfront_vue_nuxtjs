<template>
  <div class="container login">
    <div class="content1-login">
      <div class="head">
        <a class="logo" href="index.html">
          <img
            class=""
            src="~/assets/images/logo-couleur.png"
            alt="Ozamba Sports"
          />
        </a>
        <div class="title">RESET PASSWORD</div>
      </div>
      <div class="content1-form-login">
        <form action="" @submit.prevent>
          <label class="form-label">PASSWORD</label>
          <div class="field">
              <i class="icon-lock-alt"></i>
            <input
              type="password"
              required
              class="form-control"
              placeholder="Write your passwword here..."
              v-model="login.password"
            />
          </div>
          <label class="form-label">CONFIRM PASSWORD</label>
          <div class="field">
              <i class="icon-lock-alt"></i>
            <input
              type="password"
              required
              class="form-control"
              placeholder="Write your passwword here..."
              v-model="login.confirmPassword"
            />
          </div>


          <div class="form-group top">
            <button class="form-btn" @click="onLogin()">Reset Password</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component ({
  layout: 'login'
})

class RefreshToken extends Vue {
  login: any = {password: '', confirmPassword: ''}
  token: string = ''
  mounted () {
    this.token = this.$route.params.token
  }


}

export default RefreshToken
</script>