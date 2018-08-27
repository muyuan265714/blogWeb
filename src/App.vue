<template>
  <div class="home" id="blog">
    <div id="header">
      <div class="container-header">
        <section class="lf">
          <div class="head"></div>
          <span class="name name-cn">千寻瀑</span>
          <span class="name name-en">Open Your Journey !</span>
          <div class="contactMe">
            <span v-for="(item,index) in contact" :key="index" class="ctM">
                <i :class="item.url"></i>
            </span>
          </div>
        </section>
      </div>
    </div>
    <div id="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
    export default {
        data(){
            return{
                activeIndex2: '1',
                nav:"",
                contact:[
                  {
                    url:"iconfont icon-GitHub"
                  },
                  {
                    url:"iconfont icon-QQ"
                  },
                  {
                    url:"iconfont icon-weixin"
                  },
                  {
                    url:"iconfont icon-weibo"
                  },
                  {
                    url:"iconfont icon-youxiang"
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
    background: url('../public/images/header.jpg') no-repeat;
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
        background: url('../public/images/headImg.jpg') no-repeat;
        background-size: 100% 100%;

      }
      .name{
        color: #ddd;
        font-size: 1.6rem;
        text-align: center;
        display: block;
        width: 100%;
      }
      .name-cn{
        margin-top: 8px;
        font-family: "楷体";
      }
      .name-en{
        margin-top: 3px;
        font-size: 1.0rem;
      }
      .contactMe{
        padding-top: 30px;
        text-align: center;
        .ctM{
          transition: background-color 0.7s;
          display: inline-block;
          width: 35px;
          height: 35px;
          margin: 0 10px;
          border-radius: 50%;
          overflow: hidden;
          border: 1px solid #ccc;
          &:hover{
            background-color:#fff;
            .iconfont{
              color:#000;
            }
          }
          .iconfont{
            transition: color 0.6s;
            color:#fff;
            font-size: 20px;
            line-height: 35px;
          }
        }
      }
    }
  }
  #container{
    float: right;
    width: 60%;
    height: 100%;
  }
</style>

