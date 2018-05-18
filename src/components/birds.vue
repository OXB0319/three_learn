<template>
<div ref="test1">

</div>
</template>
<script>
  import THREE from "three";

  export default{

      mounted:function(){
          var scene  = new THREE.Scene();

          var camera =  new THREE.PERSPECTIVE_CAMERA(75, window.innerWidth/window.innerHeight, 0.1, 1000);

          var renderer = new THREE.WebGLRenderer();

          renderer.setSize(window.innerWidth, window.innerHeight);



      }

  }

</script>
<style>


</style>
