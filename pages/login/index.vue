<template>
  <div class="container login">
    <div class="content1-login">
      <div class="head">
        <a class="logo" href="index.html">
          <img
            class=""
            src="images/logo_symbol_trademark_sf1.png"
            alt="Ozamba Sports"
          />
        </a>
        <div class="title">CONNECT</div>
      </div>
      <div class="content1-form-login">
        <form action="">
          <br />
          <br />
          <label class="form-label">USERNAME / MAIL</label>
          <div class="field">
            <span>@</span>
            <input
              type="text"
              required
              placeholder="Write your username here..."
            />
          </div>
          <br />
          <br />
          <label class="form-label">PASSWORD</label>
          <div class="field">
            <span>
              <img src="images/lock.png" class="lock-inside-input" />
            </span>
            <input
              type="text"
              required
              placeholder="Write your passwword here..."
            />
          </div>
          <br />
          <span class="mini-label">Forgot your password?</span>

          <div class="form-group top">
            <button class="form-btn">log in</button>
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
class Login extends Vue {}

export default Login;
</script>
