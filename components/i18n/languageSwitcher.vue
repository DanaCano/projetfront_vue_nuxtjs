<template>
  <div class="language-switcher">
    <div>
      <i class="fflag fflag-FR ff-xl ff-round"></i>
    </div>
    <div class="language-list">
      <div v-for="lang in $i18n.locales" :key="lang.code" class="language-item">
        {{lang.name}}
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
@Component
class LanguageSwitcher extends Vue {
  mounted () {
  }
}
export default LanguageSwitcher
</script>