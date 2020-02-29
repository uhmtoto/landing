<script>
import Apple from '../assets/apple-logo.png'
export default {
  name: 'front',
  data () {
    return {
      Apple
    }
  }
}
</script>

<template>
  <div class='card'>
    <img class='apple-logo' :src='Apple' />
    <div class='profile'>
      <span class='name'>Seohun Uhm</span>
      <a
        href='https://jnjcomu.github.io/landing'
        class='team'
      >
        @JnJ_Comu
      </a>
      <a
        href='https://unicon-dimigo.github.io'
        class='team'
      >
        @Unicon
      </a>
    </div>
    <div class='chip'>
      <div class='chip-q'></div>
      <div class='chip-q'></div>
      <div class='chip-q'></div>
      <div class='chip-q'></div>
      <div class='chip-q'></div>
      <div class='chip-q'></div>
    </div>
    <span @click="$emit('toggle')" class='button'>
      Detail ->
    </span>
  </div>
</template>

<style scoped>
.card {
  position: relative;
  width: 30em;
  height: 40%;
  background-color: #f6f6f6;
  border-radius: 15px;
  box-shadow: 20px 20px 60px #d1d1d1, -20px -20px 60px #ffffff;
  font-family: 'Inter', sans-serif;
  font-weight: 300;
}

.apple-logo {
  position: absolute;
  top: 8%;
  left: 8%;
  height: 3.8rem;
  width: auto;
}

.profile {
  position: absolute;
  bottom: 18%;
  left: 8%;
}

.name {
  font-size: 1.4rem;
  color: #757676;
  display: block;
  margin-bottom: 1px;
}

.team {
  color: #757676;
  display: inline;
}

.button {
  position: absolute;
  bottom: 5%;
  right: 8%;
  color: #606060;
  cursor: pointer;
  user-select: none;
}

.chip {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  position: absolute;
  background-color: #f2f2f2;
  border: 1px solid #666;
  right: 8%;
  bottom: 18%;
  width: 3.7rem;
  height: 2.5rem;
  border-radius: 8px;
  padding: 1px;
  box-sizing: border-box;
}

.chip-q {
  width: 20px;
  height: 8px;
  border: 1px solid #666;
  border-radius: 10px;
}
</style>
