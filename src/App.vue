<script setup lang="ts">
import SpaceTime from './components/SpaceTime.vue';
//import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  
  <div id="slot1">
    <div id="titles">
    <h3>Quantum Visual Experiments</h3>
    </div>
    <div id="info">
      <h3>Space  Time</h3>
    <p>The fundamental concepts of classical physics, space, time, mass, and derived concepts.</p>
    </div>
  <div id="spaceContainer">
    <SpaceTime />
  </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
#slot1 {
 display: flex 2fr 2fr 2fr;
 overflow-x: hidden;
}
#titles {
  position: absolute;
	top: 100px;
  left: 100px;
	text-align: center;
	z-index: 100;
	display:block;
  color: #242526;
  background-color: rgba(255, 255, 255, 0.60);
  border-radius: 25px;
  padding: 0 30px;
}
#info {
  position: absolute;
	top: 50;
  bottom: 45%;
  left: 50;
  right: 10%;
	text-align: center;
	z-index: 100;
	display:flex;
  color: #242526;
  background-color: rgba(255, 255, 255, 0.60);
  border-radius: 25px;
  padding: 0 30px;
  max-width: 270px;
}
#info h3{
  align-self: center;
  padding-right: 5%;
}

#info p {
  font-size: small;
  align-self: center;
}
</style>
