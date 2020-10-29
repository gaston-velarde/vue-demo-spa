<template>
  <div style="margin-top:20px">
    <h1>Bindings</h1>
    <div class="row">
      <div class="col-sm-12">
        <p>{{oneWay}}</p>
      </div>
      <div class="col-sm-12">
        <div class="form-group">
          <label>Two way binding</label>
          <input v-model="twoWay" type="email" class="form-control">
        </div>
        <p>{{twoWay}}</p>
      </div>
      <div class="col-sm-12">
        <input @click="showAlert()" class="btn btn-primary" value="Click Binding">
      </div>
      <div class="col-sm-12">
        <div v-html="rawHtml()"></div>
      </div>
      <div class="col-sm-12">
        <p>Javascript expression in a html</p>
        <p>1 + 1 = {{1+1}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      oneWay: "this is a one way binding",
      twoWay: ""
    }
  },
  methods:{
    showAlert(){
      alert("I have been clicked!")
    },
    rawHtml(){
      return "<span style='color:green'>This is a binded HTML</span>"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
