<template>
  <div>
    <div class="customClass">
      <h1> This is a test page using Nuxt in Vue.js made by Alejandro Monteseirin </h1>
      <button v-on:click="sayHi"> Press Me!</button>
      {{text}}
      <br>
      <div style="text-align:center"><nuxt-logo style="height:5em"></nuxt-logo></div>
    </div>
    <div style="margin-top:5em">
      <nuxt-link to="/about">About</nuxt-link>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import NuxtLogo from '~/components/NuxtLogo.vue';

export default Vue.extend({
  components: { NuxtLogo },
  name: 'IndexPage',
  data () {
    return {
    text: "Press the button!",
    sentence: 0
    }
  },
  methods: {
    sayHi: function () {
      this.sentence++
      switch (this.sentence){
        case 0:
          this.text="Press the button!";
          break;
        case 1:
          this.text="Hi! Im changing the text reactively";
          break;
        case 2:
          this.text="I have a limited number of sentences, the next time you press the button i will reset";
          break;
        case 3:
          this.sentence=-1;
          this.sayHi();
          break;
      }


    
    
    }
  }
})
</script>
<style>
.customClass {
  margin: 20%;
  background-color: whitesmoke;
  border-radius: 3em ;
  padding: 2em;
}
</style>
