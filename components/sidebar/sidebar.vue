<template>
  <div class="sidebar">
<!--
    <span>
      <i class="icon-right-short" @click="onLogout()"></i>
    </span>
-->
  <div id="sidebar-logo" class="logo">
    <img src="~/assets/images/logo.png">
  </div>
  <ul id="sidebar-menu" class="sidebar-menu">
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-dashboard"></i>
        <span class="label">Dashboard</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-document"></i>
        <span class="label">Document</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-run"></i>
        <span class="label">Athletes</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-calendar"></i>
        <span class="label">Calendar</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-team"></i>
        <span class="label">Team</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-ok"></i>
        <span class="label">Endorsement</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-report"></i>
        <span class="label">Reports</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-medal"></i>
        <span class="label">CSR</span>
      </a>
    </li>
    <li class="list-menu">
      <a class="link-menu">
        <i class="icon-rocket"></i>
        <span class="label">Innovation</span>
      </a>
    </li>
  </ul>
  <div id="sidebar-language" class="language">
    <img class="flag" src="~/assets/images/flag-for-united-kingdom.png">
    <span class="text">Language</span>
    <i class="icon icon-chevron-right"></i>
  </div>
</div>
</template>
<script lang="ts">

import Vue from 'vue'
import Component from 'vue-class-component'
class SideBar extends Vue {
  menus: any = [];
  onLogout() {
    try {
      this.$auth.logout()
      this.$router.push('/')
    } catch (err) {

    }
  }

  data() {
    return {
      menus: [
        {icon: 'icon-dashboard', label: 'Dashboard'},
        {icon: 'icon-document', label: 'Document'},
        {icon: 'icon-run', label: 'Athletes'},
        {icon: 'icon-calendar', label: 'Calendar'}
      ]
    };
}
}
export default SideBar
</script>
