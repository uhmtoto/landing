<script>
import Front from './components/Front'
import Back from './components/Back'

export default {
  name: 'app',

  components: { Front, Back },

  data () {
    return {
      state: false
    }
  },

  methods: {
    toggleDetail () {
      this.state = !this.state
    }
  }
}
</script>

<template>
  <div class='container'>
    <Front v-if='!state' @toggle='toggleDetail' />
    <Back v-else @toggle='toggleDetail' />
  </div>
</template>

<style>
@import url('https://rsms.me/inter/inter.css');

.container {
  width: 100vw;
  height: 100vh;
  padding: 20px 8px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #D3CCE3;
  background: -webkit-linear-gradient(to right, #E9E4F0, #D3CCE3);
  background: linear-gradient(to right, #E9E4F0, #D3CCE3);
}

body {
  margin: 0;
}

a {
  text-decoration: none;
}

ul {
  list-style: none;
  padding-left: 15px;
  margin-top: 10px;
}
</style>
