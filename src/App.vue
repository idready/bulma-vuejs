<template>
  <div id="app" class="columns">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
    <!-- <HelloCode
      v-for="item in $data.groceryList"
      v-bind:todo="item"
      v-bind:key="item.id"
    /> -->
    <HeaderComponent class="column is-full is-full-mobile"/>
    <main role="main" class="column is-full is-full-height"></main>
    <FooterComponent class="column is-full is-full-mobile"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import FooterComponent from './components/core/FooterComponent.vue';
import HeaderComponent from './components/core/HeaderComponent.vue';

@Component({
  components: { HelloWorld, FooterComponent, HeaderComponent },
})
export default class App extends Vue {
  // private groceryList: Object = groceryList;
}
</script>

<style lang="scss">
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    flex-flow: row wrap;
  }

</style>
