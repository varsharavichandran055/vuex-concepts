<template>
  <base-container title="Vuex">
  <!-- <h3>{{ $store.state.counter }}</h3> -->
  <!-- <h3>{{ counter }}</h3> -->
  <the-counter></the-counter>
  <favorite-value></favorite-value>
  <button @click="addOne">Add 10</button>
  <change-counter></change-counter>
  </base-container>
 
</template>

<script>
import BaseContainer from './components/BaseContainer.vue'
import TheCounter from './components/TheCounter.vue'
import ChangeCounter from './components/ChangeCounter.vue'
import FavoriteValue from './components/FavoriteValue.vue'

export default {
  components: {
    BaseContainer,
    TheCounter,
    ChangeCounter,
    FavoriteValue
  },
  // computed:{
  //   counter(){
  //     return this.$store.state.counter;
  //   }
  // },
  methods:{
    addOne(){
      // this.$store.state.counter=this.$store.state.counter + 11;
      // this.$store.commit('increase',{value:10});
      // this.$store.commit({  //mutation example 
        this.$store.dispatch({  //action example 
      type:'increase',
      value:10
      });
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>