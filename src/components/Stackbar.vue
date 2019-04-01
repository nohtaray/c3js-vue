<template>
  <div>
    <vue-c3 :handler="handler"></vue-c3>
  </div>
</template>

<script>
import Vue from 'vue'
import VueC3 from 'vue-c3'
import 'c3/c3.min.css'

export default {
  name: 'stackbar',
  components: {
    VueC3
  },
  data () {
    return {
      handler: new Vue()
    }
  },
  mounted () {
    let options = {
      data: {
        columns: [
          ['データ1', 60, 55, 45, 40, 40, 35, 30, 30],
          ['データ2', 15, 15, 10, 10, 10, 10, 5, 0]
        ],
        type: 'bar',
        groups: [
          ['データ1', 'データ2']
        ],
        order: null, // 定義順
      },
      axis: {
        rotated: true // 横棒
      }
    }
    this.handler.$emit('init', options)
  }
}
</script>
