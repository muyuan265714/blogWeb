<template>
  <div class="home" id="blog">
    <div id="header">
      <div class="container-header">
        <section class="lf">
          <div class="head"></div>
          <span class="name">李枫</span>
          <span class="name name-en">Open your journey !</span>
        </section>
      </div>
    </div>
    <id id="container">
      <router-view></router-view>
    </id>
  </div>
</template>

<script>
    export default {
        data(){
            return{
                activeIndex2: '1',
                nav:[
                  {
                    index:"/",
                    title:"首页"
                  },
                  {
                    index:"/home",
                    title:""
                  },
                  {
                    index:"/home",
                    title:"首页"
                  },
                  {
                    index:"/home",
                    title:"首页"
                  },
                ]
            }
        },
        methods:{

        }
    }
</script>

<style lang="less">
  body{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: 0;
    padding: 0;
  }
  .home{
    height: 100%;
  }
  #header{
    background: url('./assets/images/header.jpg') no-repeat;
    background-size: 100% 100%;
    position: fixed;
    left: 0;
    top: 0;
    width: 40%;
    height: 100%;
    background-color: #eee;
    .container-header{
      background-color: rgba(0,0,0,0.4);
      width: 100%;
      height: 100%;
      padding-top: 20%;
      .head{
        width: 100px;
        height: 100px;
        margin: auto;
        background-color: #fff;
        border-radius: 50%;
        background: url('./assets/images/headImg.jpg') no-repeat;
        background-size: 100% 100%;

      }
      .name{
        color: #ddd;
        font-size: 1.6rem;
        text-align: center;
        display: block;
        width: 100%;
        margin-top: 8px;
        font-family: "微软雅黑";
      }
      .name-en{
        font-size: 1.0rem;
      }
    }
  }
  #container{
    float: right;
    width: 60%;
    height: 100%;
  }
</style>

