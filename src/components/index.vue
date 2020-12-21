<template>
  <div class="taskPlan" ref="taskPlanTimeForm" style="width:100%;height:100%">
    <iframe :src="reportUrl" frameborder="0" style="width:100%;" :height="tableHeight" id="iframeBox"></iframe>
    <div id="loginBox">
      <h4 style="color:white">登录</h4>
      <Input placeholder="Enter name" style="width: auto">
            <Icon type="ios-contact" slot="prefix" />
      </Input>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      reportUrl: "../../static/html/夜景.html",
      tableHeight:window.screen.availHeight-106.6+'px',
      loginForm: {
        userName: "",
        passWord: ""
      },
      loginRules: {
        userName: [
          { required: true, message: "请输入用户名", trigger: "blur" }
        ],
        passWord: [{ required: true, message: "请输入密码", trigger: "blur" }]
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
  margin: 0;
  width: 100%;
  height: 100%;
  background-color: black;
}
#loginBox {
    width: 240px;
    height: 280px;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    padding: 50px 40px 40px 40px;
    box-shadow: -15px 15px 15px rgb(38 6 47 / 70%);
    opacity: 1;
    background: linear-gradient( 230deg, rgb(74 72 53 / 0%) 0%, #ff33f9a6 100% );
    /deep/ .inps input {
      border: none;
      color: #fff;
      background-color: transparent;
      font-size: 12px;
    }
    .submitBtn {
      background-color: transparent;
      color: #39f;
      width: 200px;
    }
    .iconfont {
      color: #fff;
    }
  }
</style>
