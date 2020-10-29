<template>
  <div style="margin-top:20px">
    <h1>Conditional Rendering</h1>
    <div class="row">
      <div class="col-sm-12">
        <img v-if="showImage" src="https://www.gematsu.com/wp-content/uploads/2020/09/Genshin-Impact_2020_09-13-20_Top.jpg" class="img-fluid" alt="Responsive image">
        <input @click="showImage = !showImage" class="btn btn-primary" value="Toggle image">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showImage: false
    }
  },
  methods:{
  }
}
</script>

