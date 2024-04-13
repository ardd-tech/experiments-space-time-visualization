<script setup lang="ts">
import SpaceTime from './components/SpaceTime.vue';
//import HelloWorld from './components/HelloWorld.vue';
</script>

<template>



  <div id="slot1"> 
<div id="titles">
    <h3>Space | Time</h3>
    </div>
    

    <div id="info">
      <h3>Space Time</h3>
      <p>The fundamental concepts of classical physics, space, time, mass, and derived concepts.</p>
    </div>

    <!--LCARS DIVS-->
    <div id="left" class="lcars">
    <div class="lcars_btn"><h3>Quantum Visual Experiments</h3></div>
    <div class="lcars_btn"><h3>Quantum Visual Experiments</h3></div>
    <div class="lcars_btn"><h3>Quantum Visual Experiments</h3></div>
    <div class="lcars_btn"><h3>Quantum Visual Experiments</h3></div>
  </div>

  <div id="info">
      <h3>Space Time</h3>
      <p>The fundamental concepts of classical physics, space, time, mass, and derived concepts.</p>
    </div>

  <div id="spaceContainer">
    <SpaceTime />
  </div>

  </div>
  



</template>

<style scoped>
/*.logo {
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
*/
body, html{
  overflow: hidden;
  box-sizing: border-box;
}
#slot1 {
 display: flex;
 overflow: hidden !important;
 width: auto;
 height: auto;
 box-sizing: border-box;
 justify-content: center;
 align-items: center;
}
#slot1 *{
  box-sizing: border-box;
}
/*#spaceContainer{
  overflow: hidden;
  box-sizing: border-box;
  display: flex;
  width: fit-content;
  height: fit-content;
}*/
#titles {
  position: fixed;
	top: 1%;
  width: 100vw;
  left: 50%;
	text-align: center;
	z-index: 100;
	display:flex;
  align-items: center;
  
  color: white;


}
#info {
  position: fixed;
	top: 50;
  bottom: 50;
  right:5%;
	text-align: center;
	z-index: 100;
	display:flex;
  color: #242526;
  background-color: rgba(255, 255, 255, 0.60);
  border-radius: 25px;
  padding: 0 30px;
  width: 270px;
}
#info h3{
  align-self: center;
  padding-right: 5%;
}

#info p {
  font-size: small;
  align-self: center;
}
#left {
  
  position: fixed;
  left: 0;
  top: 0;
	text-align: center;
	z-index: 100;
  color: #242526;
  background-color: rgba(255, 255, 255, 0.60);
  border-radius: 0 25px 25px 0;
  padding: 0 30px;
  width: 270px;
  height: 100vh;
  
}


</style>