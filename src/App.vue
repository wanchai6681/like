
<template>
  <div id="app" class="bg-secondary ">
  <img alt="Vue logo" src="./assets/Edit.jpg" class="img-fluid white=150x150px">
      <div class="row mb-5 mt-3">
                <div class="mt-2 mr-auto ml-1 mb-2">
              
                </div>
                <div class="">
               
                </div>
                <div class="card-body">
                    <CsButton></CsButton>
                </div>
    </div>
    
  </div>
</template>

<script>
import CsButton from "./components/CsButton";
export default {
  name: "App",
  components: {
    // eslint-disable-next-line no-undef
    CsButton
  },

  data: function () {
    return {
      total: 0,
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
  color: blue;
  margin-top: 60px;
}
h3#nav {
    text-align: left;
    font-family: 'Open Sans Condensed', sans-serif;
}

.logo {
    width: 30px;
}

.logofooter {
    width: 80px;
    margin: 10px;
}

footer {
    font-family: 'Open Sans Condensed', sans-serif;
}

p.box {
    width: 150px;
    white-space:initial;
    white-space:normal;
    text-align: center;
    word-wrap: break-word;
    margin: auto;
}
.icon{
    width: 35px;
    margin: 5px;

}
</style>