<template>
  <div id="app">
    <navi></navi>
    <div>
      <span class="test">Welcome to my web</span>
      <span class="fa fa-code"></span>

      <birds style="position: absolute; top: 100px;left: 0px"></birds>
    </div>
  </div>
</template>

<script>
  import navi from './components/common/navi.vue';
  import birds from './components/birds.vue';

  export default {
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },
    components:{
        "navi":navi,
        "birds":birds
    }
  }
</script>

<style lang="scss">
  @import "assets/font-awesome-4.7.0/css/font-awesome.css";
  body{
    padding: 0;
    margin: 0;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    /*color: #2c3e50;*/
  }

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    text-decoration: none;
    color: #42b983;
  }
  .test{
    position: relative;
  }

  .test::before{
    content: "";
    position: absolute;
    left:0;
    bottom: 0;
    width: 100%;
    height: 2px;
    background: #42b983;
    -webkit-transition: transform .3s ;
    -moz-transition: transform .3s ;
    -ms-transition: transform .3s ;
    -o-transition: transform .3s ;
    transition: transform .3s ;
    transform: scaleX(0);
    transform-origin: 100% 0;
  }

  .test:hover::before{
    transform: scaleX(1);
    transform-origin: 0 0;
  }


</style>
