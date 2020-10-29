<template>
  <div style="margin-top:20px">
    <h1>List Rendering</h1>
    <div class="row">
      <div class="col-sm-12">
        <ul id="example-1">
                <li v-for="item in items" :key="item.message">
                    {{ item.message }}
                </li>
            </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
        items: [
            { message: 'Hi' },
            { message: 'Hello' },
            { message: 'Saranghe' }
        ]
    }
  },
  methods:{
  }
}
</script>

