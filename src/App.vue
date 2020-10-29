<template>
  <div class="container" id="app">
    <bindings></bindings>
    <condition></condition>
    <list-rendering></list-rendering>
    <prop :msg="msg"  @clicked="onClickChild"></prop>
  </div>
</template>

<script>
import Prop from './components/Prop'
import Condition from './components/condition'
import Bindings from './components/Bindings'
import ListRendering from './components/ListRendering'
export default {
  name: 'App',
  data(){
    return {
      msg:"I came from the parent"
    }
  },
  components: {
    Prop,
    Bindings,
    Condition,
    ListRendering
  },
  methods: {
    onClickChild(value){
      alert(value);
    }
  }
}
</script>
<style scoped>
  #app{
    margin-top: 50px;
  }
</style>