<template>
  <div class="language-switcher">
    <v-app>
      <v-menu :close-on-click="closeOnClick">
        <template v-slot:activator="{ on, attrs }">
          <v-btn v-bind="attrs" v-on="on">
            <i
              class="fflag ff-xl ff-round"
              v-bind:class="`fflag-${$i18n.getLocaleCookie().toString().toUpperCase()}`"
            ></i>
          </v-btn>
        </template>
        <v-list>
          <v-list-item v-for="lang in $i18n.locales" :key="lang.code">
            <nuxt-link :to="switchLocalePath(lang.code)">
              <v-list-item-title>
                <i
                  class="fflag ff-xl ff-round"
                  :class="`fflag-${lang.code.toUpperCase()}`"
                ></i>
                {{ lang.name }}
              </v-list-item-title>
            </nuxt-link>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
@Component
class LanguageSwitcher extends Vue {
  closeOnClick: boolean = true;
  locale: string = ''
  mounted () {
    //console.log("eto")
    //this.locale = typeof(this.$i18n.getLocaleCookie()) !== 'undefined' ? this.$i18n.getLocaleCookie()?.toString().toUpperCase() : this.$i18n.defaultLocale.toString().toUpperCase()
  }

}
export default LanguageSwitcher;
</script>