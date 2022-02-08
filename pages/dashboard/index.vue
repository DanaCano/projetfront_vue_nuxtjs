<template>
  <div>Dashboard</div>
</template>

<script>
import Vue from 'vue'
import Component from 'vue-class-component'

@Component({
  layout: 'default',
  middleware: ['auth']
})

class Dashboard extends Vue {

}

export default Dashboard
</script>
