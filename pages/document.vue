<template>
  <div>Document</div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
@Component ({
  layout: 'connected',
  middleware: ['auth']
})

class Document extends Vue {

}
export default Document
</script>