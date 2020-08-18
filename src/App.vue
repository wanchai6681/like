<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <h1>{{ total }}</h1>
    <div class="row">
      <div class="col-3">
        <counter lable="ok" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="ชอบ" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="อะหยังครับจารย์" @cc="sum" />
      </div>
      <div class="col-3">
        <counter lable="55555" @cc="sum" />
      </div>
    </div>
    ชื่อ-นามสกุล <input type="text" v-model="nam">  
    รหัส นศ  <input type="text" v-model="code"/>
    GPA <input type="number" v-model="gpa" step="0.01"/>
    {{name}}{{code}}{{GPA}}
  </div>
</template>

<script>
import HelloWorld from "/src/components/HelloWorld.vue";
import Counter from "/src/components/Counter.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    Counter,
  },

  data: function () {
    return {
      total: 0,
      name:'',
      code:'',
      GPA:0.0,
    }
  },
  methods: {
    sum(CounterValue) {
      this.total += CounterValue;
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>