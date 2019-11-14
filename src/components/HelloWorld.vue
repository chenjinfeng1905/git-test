<template>
  <div class="hello">
    <!-- <Countdown endTime="1549960618" :callback="callback" endText="已经结束了"></Countdown> -->
    <draggable v-model="list2" :move="move">
      <li v-for="(item, index) in list2" :key="index">{{item}}</li>
    </draggable>
  </div>
</template>

<script>

import Countdown from '@/components/time'
import draggable from 'vuedraggable'

export default {
  name: 'HelloWorld',

  components: {
    Countdown, draggable
  },

  data () {
    return {
      list2: [
        '张三11111', '里斯222222', '张三33333', '里斯44444'
      ]
    }
  },

  methods: {
    move: function (originalEvent) {
      console.log(originalEvent)
    }
  }
}
</script>
<style scoped>
h1, h2 {
  font-weight: normal;
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
