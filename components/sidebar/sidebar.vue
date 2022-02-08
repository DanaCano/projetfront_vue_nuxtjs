<template>
  <div>
    <button @click="onLogout()">logout</button>
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
