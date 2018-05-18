<template>
  <div ref="test1" class="container">

  </div>
</template>
<script>
  import * as THREE from "three";

  export default{
    data:()=>({
      scene:null,
      camera:null,
      renderer:null,
      geometry:null,
      material:null,
      box:[],
      cube:null
    }),
    mounted:function(){
      this.init();
      this.draw();
      this.animate();
    },

    methods:{
      init:function(){
        let scene  = new THREE.Scene();
       scene.background = new THREE.Color(0xf0f0f0);
        let camera =  new THREE.PerspectiveCamera(75, 1, 0.1, 1000);
        let renderer = new THREE.WebGLRenderer();
//        renderer.setSize(window.innerWidth, window.innerHeight);

        renderer.setSize(200,200)
        this.$refs.test1.appendChild(renderer.domElement);
        let geometry = new THREE.BoxGeometry(2,2,2);
        let material = new THREE.MeshLambertMaterial({color: 0x00ff00});
        let cube = new THREE.Mesh(geometry, material);
        this.scene = scene;
        this.camera = camera;
        this.renderer = renderer;

        this.geometry = geometry;
        this.material = material;
        this.cube = cube;
      },

      draw:function(){
          let light = new THREE.DirectionalLight(0xdddddd,1);
          light.position.set(1,1,1).normalize();
          this.scene.add(light);

        this.scene.add(this.cube);
        this.camera.position.z = 5;
        this.renderer.render(this.scene, this.camera);
      },

      animate:function(){
        requestAnimationFrame(this.animate);
        this.cube.rotation.x += 0.02;
        this.cube.rotation.y += 0.02;
        this.renderer.render(this.scene, this.camera)
      }
    }

  }

</script>
<style>
  .container{
    width: 200px;
    height: 200px;
  }

</style>
