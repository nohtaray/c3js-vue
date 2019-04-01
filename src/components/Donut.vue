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
  name: 'donut',
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
          ['データ1', 650],
          ['データ2', 320],
          ['データ3', 208],
          ['データ4', 208],
          ['データ5', 108],
          ['データ6', 58],
          ['データ7', 18]
        ],
        type: 'donut',
        order: null, // 定義順
      },
      donut: {
        title: '1400 人',
        label: {
          format: function(value, ratio, id) {
            return `${id}: ${value} 人`;
          }
        }
      }
    }
    this.handler.$emit('init', options)
  }
}
</script>
