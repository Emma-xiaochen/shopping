<template>
  <div class="personal">
    <nav-bar></nav-bar>
    <search-bar></search-bar>
    <div class="container">
      <div class="top"><div class="home">首页</div> / 个人中心</div>
      <div class="wrap">
        <div class="header">
          <div class="fl">
            <div class="head">
              <img src="@/assets/images/head.png" alt="">
            </div>
            <div class="right">
              <div class="item name">admin</div>
              <div class=" item say">您好~</div>
              <div class=" item modify-info">修改个人信息></div>
            </div>
          </div>
          <div class="fr">
            <div class="item">账户安全：<div class="value">普通</div></div>
            <div class="item">绑定手机：136******68</div>
            <div class="item">绑定邮箱：未绑定</div>
          </div>
        </div>
        <div class="content">
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-wodedingdan"></span>
            </div>
            <div class="message">
              <div class="title">我的订单：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看我的订单></div>
            </div>        
          </div>
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-daizhifu-"></span>
            </div>
            <div class="message">
              <div class="title">待支付的订单：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看待支付订单></div>
            </div>        
          </div>
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-daishouhuo"></span>
            </div>
            <div class="message">
              <div class="title">待收货的订单：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看待收货的订单></div>
            </div>        
          </div>
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-pinglun"></span>
            </div>
            <div class="message">
              <div class="title">待评价的订单：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看待评价的订单></div>
            </div>        
          </div>
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-shoucang"></span>
            </div>
            <div class="message">
              <div class="title">收藏的商品：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看收藏的商品></div>
            </div>        
          </div>
          <div class="item">
            <div class="icons">
              <span class="iconfont icon-shouhou"></span>
            </div>
            <div class="message">
              <div class="title">退还/售后的订单：<div class="num">0</div></div>
              <div class="detail" @click="goOrder">查看退还/售后的订单></div>
            </div>        
          </div>
        </div>
      </div>
    </div>
    <footer-bar></footer-bar>
  </div>
</template>

<script>
  import navBar from '@/components/navBar'
  import searchBar from '@/components/searchBar'
  import footerBar from '@/components/footerBar'

  export default {
    components: {
      navBar,
      searchBar,
      footerBar
    },
    methods: {
      goOrder() {
        this.$router.push({name: 'order'});
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import url('~@/assets/iconfont/iconfont.css');

  .personal {
    background: #f5f5f5;
    .container {
      width: 1200px;
      margin: 0 auto;
      .top,
      .home {
        display: inline-block;
      }
      .top {
        width: 100%;
        height: 41px;
        line-height: 41px;
        color: #757575;
        border-bottom: 2px solid #ff2832;
      }
      .home {
        cursor: pointer;
        &:hover {
          color: #ff2832;
        }
      }
      .wrap {
        min-height: 500px;
        background: #ffffff;
        border: 1px solid rgba(0,0,0,.1);
        margin-bottom: 20px;
        padding: 36px 48px;
        .header {
          display: flex;
          justify-content: space-around;
          align-items: center;
          height: 230px;
          border-bottom: 1px solid rgba(0, 0, 0, .1);
          .fl {
            display: flex;
            justify-content: space-around;
            align-items: center;
            .head {
              position: relative;
              width: 160px;
              height: 160px;
              border: 1px solid rgba(0, 0, 0, .1);
              border-radius: 100%;
              margin-right: 20px;
              img {
                position: absolute;
                top: 5px;
                left: 5px;
                width: 150px;
                height: 150px;
                border-radius: 100%;
              }
            }
            .right {
              .item {
                margin: 5px 0;
              }
              .name {
                font-size: 24px;
              }
              .say {
                color: #b0b0b0;
              }
              .modify-info {
                font-size: 12px;
                color: #ff2832;
                margin-top: 15px;
                cursor: pointer;
              }
            }
          }
          .fr {
            width: 260px;
            .item,
            .value {
              display: inline-block;
            }
            .item {
              margin-bottom: 10px;
              .value {
                color: #ff2832;
              }
            }
          }
        }
        .content {
          padding: 36px 100px;
          overflow: hidden;
          display: flex;
          justify-content: space-around;
          flex-wrap: wrap;
          .item {
            display: flex;
            align-items: center;
            width: 400px;
            height: 100px;
            margin-bottom: 20px;
            .icons {
              position: relative;
              width: 100px;
              height: 100px;
              margin-right: 12px;
              background: pink;
              border-radius: 100%;
              .iconfont {
                color: #ffffff;
              }
              .icon-wodedingdan {
                position: absolute;
                top: 29px;
                left: 28px;
                font-size: 45px;
              }
              .icon-daizhifu- {
                position: absolute;
                top: 25px;
                left: 26px;
                font-size: 50px;
              }
              .icon-daishouhuo {
                position: absolute;
                top: 23px;
                left: 21px;
                font-size: 55px;
              }
              .icon-pinglun {
                position: absolute;
                top: 26px;
                left: 22px;
                font-size: 55px;
              }
              .icon-shoucang {
                position: absolute;
                top: 24px;
                left: 25px;
                font-size: 52px;
              }
              .icon-shouhou {
                position: absolute;
                top: 21px;
                left: 19px;
                font-size: 60px;
              }
            }
            .message {
              .title,
              .num {
                display: inline-block;
              }
              .title {
                .num {
                  
                }
              }
              .detail {
                cursor: pointer;
                &:hover {
                  color: #ff2832;
                }
              }
            }
          }
        }
      }
    }
  }
</style>