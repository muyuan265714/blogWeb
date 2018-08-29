<template>
    <div class="articleList">
        <section class="article" v-for="(item,index) in article" :key="index">
            <div class="content">
                <div class="title">{{item.title}}</div>
                <div class="middle">
                    <span class="createDate">{{item.createDate}} 发布 | {{item.reviewNum}}条评论</span>
                </div>
                <div class="preview">{{item.preview}}</div>
            </div>
            <div class="img">
                <img :src="item.img" alt="">
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                article:[
                    {
                        title:"Vue3.0初步认识（一）",
                        createDate:"2018年08月28日",
                        reviewNum:"20",
                        preview:"第二次搭建博客，果断的决定使用最熟悉的Vue+elementUi制作，正巧前段时间学习了Vue-cli@3.0版本，在查询和使用Vue3.0文档和使用时踩了好多的坑，这里来记录和解决一下使用3.0时踩过的坑。",
                        img:require("../assets/images/logo.png")
                    },
                    {
                        title:"Vue3.0初步认识（二）",
                        createDate:"2018年08月28日",
                        reviewNum:"20",
                        preview:"第二次搭建博客，果断的决定使用最熟悉的Vue+elementUi制作，正巧前段时间学习了Vue-cli@3.0版本，在查询和使用Vue3.0文档和使用时踩了好多的坑，这里来记录和解决一下使用3.0时踩过的坑。",
                        img:require("../assets/images/logo.png")
                    },
                    {
                        title:"Vue3.0初步认识（三）",
                        createDate:"2018年08月28日",
                        reviewNum:"20",
                        preview:"第二次搭建博客，果断的决定使用最熟悉的Vue+elementUi制作，正巧前段时间学习了Vue-cli@3.0版本，在查询和使用Vue3.0文档和使用时踩了好多的坑，这里来记录和解决一下使用3.0时踩过的坑。",
                        img:require("../assets/images/logo.png")
                    },
                ]
            }
        }
    }
</script>

<style lang="less">
    body{
        font-family: -apple-system, BlinkMacSystemFont, "opensans", "Optima", "Microsoft Yahei", sans-serif;
    }
    a{
      display: inline-block;
      color:#000;
      text-decoration: none;
      transition: color .2s;
      &:hover{
          color:#409EFF;
      }
    }
    .articleList{
        height: 100%;
        width: 100%;
        box-sizing: border-box;
        background-color: #fff;
        padding-top: 30px;
        padding-left: 50px;
        overflow: hidden;
        .article{
            opacity: 0.7;
            transition: opacity .3s;
            width: 100%;
            height: 160px;
            padding: 30px 0;
            margin-top: 10px;
            background-color: #fff;
            &:hover{
                opacity: 1;
            }
            .content{
                padding-left: 20px;
                float: left;
                width: 70%;
                box-sizing: border-box;
                height: 100%;
                .title{
                    cursor: pointer;
                    color:#333;
                    font-size: 1.6rem;
                    font-weight: 700;
                    height: 35px;
                    line-height: 35px;
                    transition: color .3s;
                    &:hover{
                        color:#000;
                    }
                }
                .middle{
                    margin-top: 10px;
                    height: 20px;
                    line-height: 20px;
                    font-size: 1rem;
                    color:#999;
                    .author{
                        
                    }
                }
                .preview{
                    color:#666;
                    height: 75px;
                    padding-top: 15px;
                }
            }
            .img{
                float: left;
                width: 30%;
                height: 100%;
                img{
                    margin-top: -10px;
                    max-width: 70%;
                    max-height: 160px;
                    margin-left: 15%;
                    box-shadow: 0px 0px 10px 1px #888888;
                }
            }
        }
    }
</style>
