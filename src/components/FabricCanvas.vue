<template>
<div id="amer">
  <button v-on:click="addRect">Add Rect</button>
  <canvas id="can-el" width="500" height="500"></canvas>
</div>
</template>

<script>
import {fabric} from 'fabric';

const colorList = ['red', 'green', 'blue', 'purple', 'pink', 'brown', 'black'];
const cache = {};

export default {
  name: "FabricCanvas",
  mounted() {
    const ref = document.getElementById('can-el');
    cache.ref = new fabric.Canvas(ref);
  },
  methods: {
    addRect: () => {
      const r = new fabric.Rect({
        fill: colorList[Math.floor(Math.random() * (colorList.length + 1))],
        width: 20,
        height: 20,
      })
      cache.ref.add(r);
    },
  },
}
</script>

<style scoped>
#amer {
  border: 1px solid green;
  display: flex;
  align-items: center;
  justify-content: center;
}
#can-el {
  border: 1px solid red;
}
</style>
