<template>
  <div class="taskPlan" ref="taskPlanTimeForm" style="width:100%;height:100%">
    <iframe :src="reportUrl" frameborder="0" style="width:100%;" :height="tableHeight" id="iframeBox"></iframe>
    <div id="loginBox">
      <Avatar src="../../static/img/sd.png" style="margin-left: 40%;" />
      <Input v-model="userName" placeholder="Enter name" style="width: auto;margin-top:10px;background-color: transparent;">
          <Icon type="ios-contact" slot="prefix" />
      </Input>
      <Input v-model="passWord" type="password" password placeholder="Enter password" style="width: auto;margin-top:10px;background-color: transparent;">
          <Icon type="md-lock" slot="prefix" />
      </Input>
      <Button type="default" ghost long style="margin-top:30px" @click="test">Login</Button>
    </div>
    <audio class="audio" src="../../static/mp3/zsj.mp3" controls autoplay="autoplay" hidden="true"></audio>
    <Modal
        v-model="modal1"
        title="提示"
        @on-ok="ok"
        @on-cancel="cancel">
        <p><u style="color: #e60bc1;margin-left: 30px;font-weight: 600;">紫莹</u>同学专属网站,请输入正确的用户名/密码！！！</p>
        <div slot="footer">
            
        </div>
    </Modal>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      reportUrl: "../../static/html/夜景.html",
      tableHeight:window.screen.availHeight-110.6+'px',
      userName: "",
      passWord: "",
      modal1:false
    }
  },
  mounted() {
	 // 播放音乐
    
  },
  methods: {
    test(){
      if(this.userName==="紫莹" && this.passWord==="991208"){
        //this.$router.push({ path:'../../static/html/互动星空.html'});
        //window.open("../../static/html/互动星空.html")
        //window.location.href="../../static/html/互动星空.html";
        // window.location.href="../../static/html/index.html";
        window.location.href="../../static/html/index_sy.html";
      }else{
        this.modal1=true;
      }
    },
    audioAutoPlay() {
      let audio = document.getElementById("audio");
      audio.play();
      document.removeEventListener("touchstart", this.audioAutoPlay);
    }
  },
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
.ivu-input-with-prefix {
    padding-left: 32px;
    background-color: transparent;
    color: #fff;
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
    
    .submitBtn {
      background-color: transparent;
      color: #39f;
      width: 200px;
    }
    .iconfont {
      color: #fff;
    }
  }

  .inps {
    border: none;
    color: #fff;
    background-color: transparent;
    font-size: 12px;
  } 
</style>
