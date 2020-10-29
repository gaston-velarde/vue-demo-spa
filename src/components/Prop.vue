<template>
  <div>
    <h1>Data passing</h1>
    <div style="margin-top:20px" class="row">
      <div class="col-sm-12">
        <p>This is how to pass a data to child</p>
        <p>{{msg}}</p>
      </div>
      <div class="col-sm-12">
        <div class="form-group">
          <label>Pass Data back to parent</label>
          <input v-model="data" type="email" class="form-control">
        </div>
        <button @click="returnToParent()" class="btn btn-primary mb-2">Submit</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    msg: String
  },
  data(){
    return{
      data: ""
    }
  },
  methods:{
    returnToParent(){
      this.$emit('clicked', this.data)
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
