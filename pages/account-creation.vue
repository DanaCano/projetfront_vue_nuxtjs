<template>
  <div id="main-content" class="create-new-account-container main-content2">
    <div class="create-new-account-middle-1 bckgd-middle-1">
      <div id="masthead" class="header">
        <NuxtLink class="logo" to="/">
          <img class src="~/assets/images/logo.png" alt="Ozamba Sports" />
        </NuxtLink>
      </div>
      <div class="container">
        <div class="content1">
          <h1 class="title">
            WELCOME
            <br />
            <span class="sub-title">ZEUS</span>
          </h1>
          <p class="btn-group">
            <NuxtLink to="/login" name="login" class="btn-login">
              <i class="icon-dashboard"></i>
              <span class="text-login">ENTER</span>
            </NuxtLink>
          </p>
        </div>
      </div>
      <!-- end home container -->
    </div>

    <div class="create-new-account-middle-2 bckgd-middle-2">
      <div id="dashboard-content" class="dashboard-content">
        <div id="dashboard-header-content" class="header custom-header">
          <div id="dashboard-group-head-content" class="head dashboard-group-head-content">
            <!-- group-icons -->
            <div id="dashboard-group-head-icon" class="group-icon">
              <!-- icon-comment -->
              <i class="icon icon-comment-discussion"></i>
              <!-- group-icons-notifications -->
              <div id="group-icon-notification" class="group-icon-notification">
                <!-- icon-notification -->
                <i class="icon icon-notification"></i>
                <i class="icon icon-bull-empty bull"></i>
              </div>

              <!-- group-search -->
              <div id="dashboard-group-input">
                <i class="icon-search"></i>
                <input id="dashboard-search-input" type="text" placeholder="SEARCH ..." />
              </div>

              <!-- group-profile -->
              <div id="dashboard-group-profile" class="dasboard-group-profile">
                <img src="~/assets/images/profile.png" class="profile" />
                <button id="btn-profile" class="btn-profile">
                  <span>CAMILLE</span>
                  <i class="icon-chevron-down"></i>
                </button>
              </div>
            </div>
          </div>
          <!-- end group head content -->
        </div>
        <!-- end header content -->

        <div id="create-new-account-main-content">
          <div class="head">
            <h3 class="title">CREATE A NEW ACCOUNT</h3>
          </div>
          <div class="forms">
            <div class="category">
              <form class="create-new-account-form">
                <div class="category-title">Choose the category</div>
                <div class="category-group-radio-button">
                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category1"
                      class="form-category-choice"
                      value="hermes"
                    />
                    <label class="form-category-choice" for="category1">hermes</label>
                  </div>

                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category2"
                      class="form-category-choice"
                      value="mercury"
                    />
                    <label class="form-category-choice" for="category2">mercury</label>
                  </div>

                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category3"
                      class="form-category-choice"
                      value="janus"
                    />
                    <label class="form-category-choice" for="category3">janus</label>
                  </div>

                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category4"
                      class="form-category-choice"
                      value="devoir"
                    />
                    <label class="form-category-choice" for="category4">devoir</label>
                  </div>

                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category5"
                      class="form-category-choice"
                      value="coequipier"
                    />
                    <label class="form-category-choice" for="category5">coéquipier</label>
                  </div>

                  <div class="form-group-radio">
                    <input
                      type="radio"
                      hidden
                      name="category"
                      id="category5"
                      class="form-category-choice"
                      value="DEVOIR"
                    />
                    <label class="form-category-choice" for="category5">invité</label>
                  </div>
                </div>
                <div class="create-new-account-form-content">
                  <div class="form-grp-input">
                    <div class="category-title">Name</div>
                    <div class="field custom-field">
                      <i class="icon-profile"></i>
                      <input
                        type="text"
                        class="form-control"
                        placeholder="Write your username here..."
                      />
                    </div>
                  </div>

                  <div class="form-grp-input">
                    <div class="category-title">Last name</div>
                    <div class="field custom-field">
                      <i class="icon-profile"></i>
                      <input
                        type="text"
                        class="form-control"
                        placeholder="Write your last name here..."
                      />
                    </div>
                  </div>

                  <div class="form-grp-input">
                    <div class="category-title">Username</div>
                    <div class="field custom-field">
                      <i class="icon-arobase"></i>
                      <input
                        type="text"
                        class="form-control"
                        placeholder="Write your username here..."
                      />
                    </div>
                  </div>

                  <div class="form-grp-input">
                    <div class="category-title">Adress Email</div>
                    <div class="field custom-field">
                      <i class="icon-arobase"></i>
                      <input
                        type="text"
                        class="form-control"
                        placeholder="Write your address email here..."
                      />
                    </div>
                  </div>

                  <div class="form-grp-input">
                    <div class="category-title">Password</div>
                    <div class="field custom-field">
                      <i class="icon-lock-alt"></i>
                      <input
                        type="password"
                        class="form-control"
                        placeholder="Write your password here..."
                      />
                    </div>
                  </div>

                  <div class="form-grp-input">
                    <div class="category-title">Confirm Password</div>
                    <div class="field custom-field">
                      <i class="icon-lock-alt"></i>
                      <input
                        type="password"
                        class="form-control"
                        placeholder="Write your address email here..."
                      />
                    </div>
                  </div>

                  <div class="form-group custom-form-group">
                    <button class="form-btn">confirm</button>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>

      <!-- end content -->
    </div>
    <!-- group chat and bubble & login time  -->
    <i class="icon-chat-bubble chat-bubble"></i>
    <div class="login-time custom-login-time">
      <Time></Time>
    </div>
    <!-- end register container -->
  </div>
</template>
<script lang="ts">
import Vue from "vue";

class DefaultPage extends Vue {
  mounted() {
    if (this.$auth.loggedIn) {
      this.$router.push('/dashboard')
    }

  }

}

export default DefaultPage
</script>