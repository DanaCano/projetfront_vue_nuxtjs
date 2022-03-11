<template>
  <div class="sidebar">
    <span>
      <i class="icon-right-short" @click="onLogout()"></i>
    </span>
    <div class="bottom">
      <ul id="openPopup" class="menu-flag myPopup">
          <a href="#close" title=" Close" class="close">X</a>
          <li class="menu-flag-item">
              <a class="menu-flag-link" href="">
                  <img class="menu-flag-icon" src="../../assets/images/flag/emojione_flag_for_united_kingdom.svg"><span>English</span>
              </a>
          </li>
          <li class="menu-flag-item">
              <a class="menu-flag-link" href="">
                  <img class="menu-flag-icon" src="../../assets/images/flag/emojione_flag-for_st_martin.svg"><span>French</span>
              </a>
          </li>
          <li class="menu-flag-item">
              <a class="menu-flag-link" href="">
                  <img class="menu-flag-icon" src="../../assets/images/flag/emojione_flag_for_spain.svg"><span>Spanish</span>
              </a>
          </li>
          <li class="menu-flag-item">
              <a class="menu-flag-link" href="">
                  <img class="menu-flag-icon" src="../../assets/images/flag/emojione_flag_for_portugal.svg"><span>Portuguese</span>
              </a>
          </li>
          <li class="menu-flag-item">
              <a class="menu-flag-link" href="">
                  <img class="menu-flag-icon" src="../../assets/images/flag/emojione_flag_for_italy.svg"><span>Italian</span>
              </a>
          </li>
      </ul>
      <a href="#openPopup"><img src="../../assets/images/flag/emojione_flag_for_united_kingdom.svg" alt=""></a>
    </div>
  </div>
</template>
<script lang="ts">

import Vue from 'vue'
import Component from 'vue-class-component'
class SideBar extends Vue {
  onLogout() {
    try {
      this.$auth.logout()
      this.$router.push('/')
    } catch (err) {

    }
  }
}
export default SideBar
</script>
