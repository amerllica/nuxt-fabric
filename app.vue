<template>
    <Topbar />
    <FabricCanvas />
</template>

<script>
import Topbar from "./src/components/Topbar";
import FabricCanvas from "./src/components/FabricCanvas";

export default {
  components: {FabricCanvas, Topbar}
}
</script>

<style>
#__nuxt {}
</style>
