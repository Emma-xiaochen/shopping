<template>
  <div class="login">
    <div class="nav"><img src="~@/assets/images/logo.png" alt=""></div>
    <div class="container">
      <div class="main">
        <div class="fl"><img src="~@/assets/images/login_propagate.png" alt=""></div>
        <div class="fr">
          <div class="title">登录</div>
          <div class="content">
            <div class="item">
              <input type="text" placeholder="手机号/昵称/邮箱">
            </div>
            <div class="item">
              <input type="password" placeholder="密码">
            </div>
            <div class="item info">
              登陆即同意 <a href="#">用户协议、隐私政策</a>
            </div>
            <div class="item">
              <button class="login-btn">登录</button>
            </div>
            <div class="item">
              <a class="register" href="#">立即注册</a>
              <a class="forget" href="#">忘记密码</a>
            </div>
          </div>
        </div>
      </div>
      <div class="footer">
        <img src="~@/assets/images/footer.png" alt="">
      </div>
      </div>
  </div>
</template>

<script>
  export default {

  }
</script>

<style lang="scss" scoped>
  .login {
    .nav {
      width: 1200px;
      margin: 0 auto;
      padding-top: 40px;
      // line-height: 100px;
    }
    .container {
      width: 1200px;
      margin: 0 auto;
      .main {
        height: 500px;
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin-top: 80px;
        .fl {
            margin-left: -10px;
          img {
            width: 680px;
            height: 530px;
            border-radius: 30px;
          }
        }
        .fr {
          width: 420px;
          height: 400px;
          border-radius: 10px;
          box-shadow: 0 6px 20px rgba(0, 0, 0, .1);
          margin-left: 80px;
          .title {
            height: 100px;
            line-height: 100px;
            font-size: 20px;
            color: #333;
            font-weight: bold;
            text-align: center;
          }
          .content {
            // margin: 10px;
            text-align: center;
            .item {
              margin-bottom: 20px;
              input {
                width: 340px;
                height: 50px;
                font-size: 16px;
                background: #f9f9f9;
                border: 0;
                padding-left: 10px;
              }
              .login-btn {
                width: 340px;
                height: 50px;
                font-size: 18px;
                text-align: center;
                color: #fff;
                background-image: linear-gradient(90deg,#fe5447,#f3344a);
                border: 0;
                border-radius: 5px;
                box-shadow: 0 3px 8px 1px rgb(235 28 49 / 22%);
              }
              .register,
              .forget {
                width: 100px;
                display: inline-block;
                font-size: 13px;
                color: #626262;
                text-decoration: none;
              }
              .register {
                position: relative;
              }
              .register:after {
                content: '';
                display: inline-block;
                width: 1px;
                height: 12px;
                background: rgba(0, 0, 0, .2);
                position: absolute;
                top: 3px;
                right: 0;
              }
            }
            .info {
              font-size: 13px;
              color: #908e8f;
              a {
                color: #151515;
                text-decoration: none;
              }
            }
          }
        }
      }
      .footer {
        margin-top: 20px;
        padding: 50px 0 50px 170px;
      }
    }

  }
</style>