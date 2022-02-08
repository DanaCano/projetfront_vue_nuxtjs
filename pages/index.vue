<template>
  <div id="container-fluid">
    <div id="masthead" class="header">
      <a class="logo" href="index.html">
        <img class="" src="~/assets/images/logo.png" alt="Ozamba Sports" />
      </a>
    </div>
    <div class="container">
      <div class="content1">
        <h1 class="title">
          WELCOME TO<br />
          <span class="sub-title">OZAMBA SPORTS</span>
        </h1>
        <p class="btn-group">
          <NuxtLink to="/login" class="btn-login">
            <i class="icon-profile"></i>
            <span class="text-login">LOGIN</span>
          </NuxtLink>
          <a class="btn-new-account" href="#create_new_account">
            <i class="icon-plus"></i>
            <span class="text-new-account">CREATE NEW ACCOUNT</span>
          </a>
        </p>
      </div>
    </div>
    <!-- end home container -->
    <Time></Time>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

class DefaultPage extends Vue {
  mounted () {
    if (this.$auth.loggedIn) {
      //this.$router.push('/dashboard')
    }
  }
}

export default DefaultPage
</script>
