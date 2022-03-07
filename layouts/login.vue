<template>
  <div id="login-layout">
    <div class="fake-sidebar">
      <language-switcher :position="'right'"></language-switcher>
    </div>
    <div class="login-content">
      <div id="masthead" class="header">
        <div class="head">
          <NuxtLink to="/">
            <span class="icon-chevron-left icon-back"></span>
            <span class="text-back">BACK</span>
          </NuxtLink>
        </div>
      </div>
      <Nuxt />
      <div class="login-time">
        <Time></Time>
      </div>
    </div>
  </div>
</template>