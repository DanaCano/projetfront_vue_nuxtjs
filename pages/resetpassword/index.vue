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
          <br />
          <br />
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
          <div class="form-group top">
            <button class="form-btn" @click="onLogin()">Send request</button>
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
  layout: "login"
})

class ResetPassword extends Vue {
  login: any = {username: ''}
}
export default ResetPassword
</script>
