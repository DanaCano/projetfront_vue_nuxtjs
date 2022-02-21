<template>
  <div class="language-switcher">
    <div class="language-button" @click="showSwitcher = !showSwitcher">
      <i
        class="fflag ff-xl ff-round"
        v-bind:class="`fflag-${locale.toUpperCase()}`"
      ></i>
    </div>
    <div class="language-list" v-if="showSwitcher">
      <div v-for="lang in $i18n.locales" :key="lang.code" class="language-item">
        <span @click="locale = lang.code">
          <nuxt-link :to="switchLocalePath(lang.code)">
            <i
              class="fflag ff-xl ff-round"
              :class="`fflag-${lang.code.toUpperCase()}`"
            ></i>
            {{ lang.name }}
          </nuxt-link>
        </span>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
class LanguageSwitcher extends Vue {
  showSwitcher: boolean = false;
  locale: string = ''
  mounted() {
    this.locale = this.$i18n.defaultLocale
  }
}
export default LanguageSwitcher;
</script>