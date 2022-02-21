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
        <ValidationObserver ref="form">
          <form action="" @submit.prevent>
            <label class="form-label">USERNAME / MAIL</label>

            <ValidationProvider
              vid="email"
              rules="required"
              v-slot="{ errors }"
            >
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
              <span class="error-msg">{{ errors[0] }}</span>
            </ValidationProvider>
            <label class="form-label">PASSWORD</label>
            <ValidationProvider
              vid="password"
              rules="required"
              v-slot="{ errors }"
            >
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
              <span class="error-msg">{{ errors[0] }}</span>
            </ValidationProvider>
            <span class="mini-label">
              <NuxtLink 
                to="/recuperation" 
                name="resetpassword"
              >
                Forgot your password?
              </NuxtLink>
            </span>

            <div class="form-group top">
              <button class="form-btn" @click="onLogin()">log in</button>
            </div>
          </form>
        </ValidationObserver>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { Component } from "vue-property-decorator";
import { ValidationObserver, ValidationProvider } from "vee-validate";
@Component({
  layout: "login",
  components: {
    ValidationObserver,
    ValidationProvider,
  },
})
class Login extends Vue {
  login: any = { username: "", password: "" };
  mounted() {
    if (this.$auth.loggedIn) {
      this.$router.push("/dashboard");
    }
  }
  async onLogin() {
    try {
      await this.$auth.loginWith("local", { data: this.login });
      if (this.$auth.loggedIn) {
        this.$router.push("/dashboard");
      }
    } catch (err: any) {
      if (err.response.data.code === 401) {
        // @ts-ignore
        this.$refs.form.setErrors({
          email: ["E-mail or password error"],
          password: ["Password error"],
        });
      }
    }
  }
}

export default Login;
</script>
