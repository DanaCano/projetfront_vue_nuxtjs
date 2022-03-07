<template>
  <div class="language-switcher">
    <div class="language-button" @click="showSwitcher = !showSwitcher" v-click-outside="hideSwitcher">
      <i
        class="fflag ff-md ff-round"
        v-bind:class="`fflag-${$i18n
          .getLocaleCookie()
          .toString()
          .toUpperCase()}`"
      ></i>
    </div>
    <div class="language-list" v-if="showSwitcher" v-bind:class="`${position}`">
      <div v-for="lang in $i18n.locales" :key="lang.code" class="language-item">
        <span @click="locale = lang.code">
          <nuxt-link :to="switchLocalePath(lang.code)">
            <v-list-item-title>
              <i
                class="fflag ff-md ff-round"
                :class="`fflag-${lang.code.toUpperCase()}`"
              ></i>
              <span v-bind:class="{'bold':$i18n.getLocaleCookie() == lang.code}">{{ lang.name }}</span>
            </v-list-item-title>
          </nuxt-link>
        </span>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Prop } from "vue-property-decorator";
@Component
class LanguageSwitcher extends Vue {
  closeOnClick: boolean = true
  showSwitcher: boolean = false
  locale: string = ""
  @Prop() position: string
  mounted() {
    console.log(this.position)
    //console.log("eto")
    //this.locale = typeof(this.$i18n.getLocaleCookie()) !== 'undefined' ? this.$i18n.getLocaleCookie()?.toString().toUpperCase() : this.$i18n.defaultLocale.toString().toUpperCase()
  }
  hideSwitcher() {
    this.showSwitcher = false
  }
}
export default LanguageSwitcher;
</script>