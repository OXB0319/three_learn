<template>
  <div class="header">
    <div class="front">
      <a class="fa fa-github" title="github"></a>
    </div>
    <div class="middle"></div>
    <div class="right">
      <ul class="menu">
        <li class="menu-item">
            <a href="https://blog.csdn.net/ou4582850" target="_blank">作者博客</a>
        </li>
        <li class="menu-item">
          <span class="fa fa-id-card" title="作者信息"></span></li>
        <li class="menu-item">33</li>
        <li class="menu-item">33</li>
      </ul>
    </div>
  </div>
</template>
<script>

  export default{
      name:"navi",
      data:function(){
          return {

          }
      }
  }

</script>
<style lang="scss">
  a{
    cursor: pointer;
    text-decoration: none;
  }
  .header{
    display: flex;
    background-color: #24292e;
    padding-top:12px;
    padding-bottom: 12px;

    .front{
      width:30%;
      color:red;
      font-size: 2.3em;
    }

    .middle{
      width: 40%;
      color:blue;
    }

    .right{
      width: 30%;
    }

    .menu{
      display: flex;
    }

    .menu-item{
      position: relative;
      color:#c8c9ca;
      display: flex;
      cursor: pointer;
    }


    .menu-item::before{
      content: "";
      position: absolute;
      left:0;
      bottom: -10px;
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

    .menu-item:hover::before{
      transform: scaleX(1);
      transform-origin: 0 0;
    }

    .menu-item:hover{
      color:white;
    }


  }




</style>
