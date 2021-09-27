<template>
  <div id="app">
    <div>
      <input-model @catchItem="sendItem"></input-model>
      <ul v-for="(item, index) in items" v-bind:key="index">
        <list-model :item="item"></list-model>
      </ul>
    </div>
  </div>
</template>

<script>

import InputModel from './components/InputModel.vue'
import ListModel from './components/ListModel.vue'

export default {
  name: 'app',
  data(){
    return{
      items:[]
    }
  },
  methods:{
    sendItem(itemPlaceholder){      
      this.items.push(itemPlaceholder);
    }
  },
  components: {InputModel,ListModel }
}
</script>

<style> 

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>