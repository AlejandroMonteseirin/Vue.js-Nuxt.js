<template>
  <div>
    <h1>This is a about page in Vue.js using NUXT.js</h1><Nuxt-logo></Nuxt-logo>
  </div>
</template>

<script lang="ts">

import Vue from 'vue'
import NuxtLogo from '~/components/NuxtLogo.vue'

export default Vue.extend({
  components: { NuxtLogo },
  name: 'About'
})
</script>
