<script setup lang="ts">
import { TresCanvas, useRenderLoop } from '@tresjs/core';
import { shallowRef} from 'vue';
import { MapControls, Stars, Line2} from '@tresjs/cientos';
import { DoubleSide } from 'three';

const yRotate = shallowRef(0);
const obRotate = shallowRef(1);
const camPos = shallowRef(2);
//const obPos = shallowRef(3);
useRenderLoop().onLoop(({delta}) => {
    yRotate.value += 0.02 * delta;
    obRotate.value += -0.5 * delta;
    camPos.value -= 0.5 * delta;
    //obPos.value += -0.55 * delta;
});
//imports onMounted from vue
/*import { onMounted } from 'vue';
//allows dimensions to be set each time component is rendered
onMounted(() => {
    const expCanvas = document.getElementById('canvas');
    if (expCanvas) {
        expCanvas.style.width = '800px';
        expCanvas.style.height = '500px';
    }
});
*/

import { onMounted } from 'vue';
onMounted(() => {
   const expCanvas = document.getElementById('canvas') ;
   if (expCanvas) {
        expCanvas.style.width = '1200px';
        expCanvas.style.height = '500px';
   }
});

</script>

<template>
    <TresCanvas id="canvas" :window-size="false" :shadows="true" clear-color="#242526" :transparent="true" >
        <TresAmbientLight 
            point
        />
        
        <TresPerspectiveCamera :visible="true" :position="[3, 7.5, 12]" />
        <Line2
        :points="[[0, 0, 0], [3, 1.58, 0], [5, 0.8660, 0]]"
        :line-width="10"
        color="#82dbc5"
        />
        <Stars
            :count="20000"
            :rotation="[0, yRotate, 0]"
         />

        <MapControls />
        <TresMesh :position="[3,3,0]" :transparent="false">
            <TresSphereGeometry :scale="[0.5, 0.5, 0.5]"/>
            <TresMeshPhysicalMaterial color="red" />
            <DoubleSide />
        </TresMesh>
        <TresGridHelper>
            <TresMeshBasicMaterial color="white" />
        </TresGridHelper>

    </TresCanvas>
</template>

<style scoped>
</style>