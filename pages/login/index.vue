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
        <div class="title">CONNECT</div>
      </div>
      <div class="content1-form-login">
        <form action="" @submit.prevent>
          <label class="form-label">USERNAME / MAIL</label>
          <div class="field">
            <i class="icon-arobase"></i>
            <input
              type="text"
              class="form-control"
              required
              placeholder="Write your username here..."
              v-model="login.username"
            />
          </div>
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
          <span class="mini-label"><NuxtLink to="/resetpassword" name="resetpassword">Forgot your password?</NuxtLink></span>

          <div class="form-group top">
            <button class="form-btn" @click="onLogin()">log in</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Component } from "vue-property-decorator";
@Component({
  layout: "login",
})
class Login extends Vue {
  login: any = {username: '', password: ''}
  mounted () {
    if (this.$auth.loggedIn) {
      this.$router.push('/dashboard')
    }
  }
  async onLogin() {
    try {
      const log = await this.$auth.loginWith('local', {data: this.login})
      if(this.$auth.loggedIn) {
        this.$router.push('/dashboard')
      }
    } catch(err) {
      console.error(err)
    }
  }
}

export default Login;
</script>
