<template>
  <div class="login-wrap">
    <div class="login-form-wrap">
      <div class="login-head">
        <img src="./logo_index.png" alt="黑马头条号">
      </div>
      <div>
        <el-form ref="form" :model="form">
          <el-form-item prop="mobile">
            <el-input v-model="form.mobile" placeholder="请输入手机号哦"></el-input>
          </el-form-item>
          <el-form-item prop="code">
          <!-- 支持栅格布局，一共24列 -->
            <el-col :span="13">
              <el-input v-model="form.code" placeholder="请输入验证码"></el-input>
            </el-col>
            <el-col :span="7" :offset="2">
              <el-button type="primary" plain>获取验证码</el-button>
            </el-col>
          </el-form-item>
          <el-form-item prop="checked">
            <el-checkbox v-model="form.checked"></el-checkbox>
            <span>我已阅读并同意<a href="#">用户协议</a>和<a href="#">服务条款</a></span>
          </el-form-item>
          <el-form-item>
            <!-- 给组件加class  会作用到它的根元素 -->
            <el-button class="btn-login"
            type="primary"
            >登录</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data () {
    return {
      form: {
        mobile: '',
        code: '',
        checked: ''
      }
    }
  },
  methods: {}
}
</script>

<style lang="less"  scoped>
.login-wrap {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background: url('cxk2.gif')
}
.login-form-wrap {
  background: rgba(255, 255, 255, 0.4);
  padding: 30px 20px 0px 20px;
  border-radius: 8px;
}
.login-head {
  display: flex;
  justify-content: center;
  margin-bottom: 10px;
}
.el-checkbox {
  margin-left: 20px;
  margin-right: 15px;
}
.btn-login {
  width: 100%;
}
</style>
