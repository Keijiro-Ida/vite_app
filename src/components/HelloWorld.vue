<template>
  <div class="alert alert-primary">
      <h1>{{data.title}}</h1>
      <p class="mt-3 h5">{{ $store.state.message}}</p>
      <hr>
      <div class="btn btn-secondary"
        @click="$store.commit('doit')">
      <a class="h5" @click.stop="$store.commit('reset')">
        clicked: {{ $store.state.counter }}
      </a>
      </div>
  </div>

</template>

<script>
import { ref, reactive} from 'vue'

export default {
  setup(props) {
    const data = reactive({
      title: 'Vuex',
    })
    return {
      data
    }
  }
}
</script>

<style>
.area {
    width:300px;
  height:100px;
  background-color: #fff;
  padding:10px;
  font-size:20pt;
}
pre {
  font-size:16pt;
  line-height: 1.25;
}
div.out {
  padding: 0px;
  background-color: #eee;
  width:300px;
  height:200px;
}
div.mid {
  padding: 0px;
  background-color: #ddd;
  width:200px;
  height:170px;
}
div.in {
  padding: 0px;
  background-color: #ccc;
  width:100px;
  height:140px;
}
</style>
