<template>
  <div class="container login">
    <div class="content1-login">
      <div class="head">
        <span class="logo">
          <img
            class=""
            src="~/assets/images/logo-couleur.png"
            alt="Ozamba Sports"
          />
        </span>
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
              v-model="form.password"
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
              v-model="form.confirmPassword"
            />
          </div>

          <div class="form-group top">
            <button class="form-btn" @click="onReset()">Reset Password</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component({
  layout: "login",
})
class RefreshToken extends Vue {
  form: any = { password: "", confirmPassword: "" };
  isValidToken: boolean = false;
  token: string = "";
  mounted() {
    this.token = this.$route.params.token;
  }
  onReset() {
    this.form.password = this.form.password.trim();
    this.form.confirmPassword = this.form.password.trim();
    if (this.form.password === this.form.confirmPassword) {
      this.$axios
        .$post(
          `${process.env.URL_API}forgot_password/${this.$route.params.token}`,
          { password: this.form.password }
        )
        .then((res) => {
          this.$router.push("/login");
        });
    }
  }
}

export default RefreshToken;
</script>