<template>
  <div class="time">
    <div class="item-time">
      <div class="icon-container">
        <i class="icon-clock"></i>
      </div>
      <div class="text-time">
        <span class="local-time">LOCAL TIMES PARIS</span>
        <span class="hour-time">{{timeParis}}</span>
      </div>
    </div>
    <div class="item-time">
      <div class="icon-container">
        <i class="icon-clock"></i>
      </div>
      <div class="text-time">
        <span class="local-time">LOCAL TIMES PARIS</span>
        <span class="hour-time">{{timeParis}}</span>
      </div>
    </div>
    <div class="item-time">
      <div class="icon-container">
        <i class="icon-clock"></i>
      </div>
      <div class="text-time">
        <span class="local-time">LOCAL TIMES PARIS</span>
        <span class="hour-time">{{timeParis}}</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
@Component
class Time extends Vue {
  timeParis: string = ''
  created () {
    this.getTime()
    
  }
  async getTime() {
    await this.$axios.$get("http://worldtimeapi.org/api/timezone/Europe/Paris").then(res => {
      const time = new Date(res.datetime.split('.')[0])
      this.timeParis = ("0" + time.getHours()).slice(-2) + ":" + ("0" + time.getMinutes()).slice(-2)
    })
    setTimeout(() => {
      this.getTime()
    }, 5000);
  }
}
export default Time
</script>