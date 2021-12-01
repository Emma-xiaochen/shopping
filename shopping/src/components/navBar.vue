<template>
  <div class="nav-bar">
    <div class="top">
        <div class="nav-container">
          <div class="item" @click="personal">个人中心</div>
          <div class="item" @click="order">我的订单</div>
          <span class="user">admin</span>
          <div class="item">退出</div>
        </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      personal() {
        this.$router.push('personal');
      },
      order() {
        this.$router.push('order');
      }
    }
  }
</script>

<style lang="scss">
  .nav-bar {
    .top {
      background: rgb(249, 249, 249);
      padding: 8px 0;
      .nav-container {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        width: 1200px;
        margin: 0 auto;
        .item {
          color: #6e6e6e;
          padding: 0 8px 0 9px;
          cursor: pointer;
          &:hover {
            color: #ff2832;
          }
        }
        a {
          position: relative;
          color: #6e6e6e;
          text-decoration: none;
          padding: 0 8px 0 9px;
          &:hover {
            color: #ff2832;
          }
        } 
        span {
          padding-left: 8px;
        }
        a:after {
          content: '';
          display: inline-block;
          width: 1px;
          height: 12px;
          background: rgba(0, 0, 0, .2);
          position: absolute;
          top: 6px;
          right: 0;
        }
      }
    }
  }
</style>