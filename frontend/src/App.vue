<template>
      <h1 class="text-3xl font-bold underline">
      Hello World
    </h1>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue"
export default {
  data() {
    return {
      fronteEnd: null
    }
  },
  components:{
    HelloWorld
  }
}
</script>
<style>
  h1 {
    color: red;
  }
</style>
