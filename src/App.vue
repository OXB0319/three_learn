<template>
  <div id="app">
    <div>
      <div class="test">Welcome to my web</div>
      <i class="fa fa-code"></i>

      <h2>Ecosystem</h2>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>

<style lang="scss">
  @import './assets/fontawesome-free-5.0.13/web-fonts-with-css/scss/fontawesome.scss';
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
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
