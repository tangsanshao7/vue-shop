<template>
  <a-layout>
    <a-layout-header></a-layout-header>
    <a-layout-content>
      <a-row>
        <a-col :span="6" :offset="9">
          <!-- 表单开始 -->
          <a-form>
            <!-- 标题开始 -->
            <a-row class="login-title">
              <a-col :span="24">
                <h2><img src="../assets/logo.png" alt="" /> Manage System</h2>
                <span> Manage System是电商后台管理系统</span>
              </a-col>
            </a-row>
            <!-- 标题结束 -->
            <!-- 登陆方式开始 -->

            <a-row class="login-form">
              <a-col :span="24">
                <a-tabs :tabBarStyle="{ textAlign: 'center' }">
                  <!-- 账号密码登陆开始 -->
                  <a-tab-pane key="1" tab="账号密码登陆">
                    <!-- 用户名 -->
                    <a-form-item :wrapperCol="{ span: 24 }" name="username">
                      <a-input
                        size="large"
                        type="username"
                        placeholder="请输入用户名"
                      >
                        <template #prefix
                          ><UserOutlined style="color:rgba(0,0,0,.25)"
                        /></template>
                      </a-input>
                    </a-form-item>
                    <!-- 密码 -->

                    <a-form-item :wrapperCol="{ span: 24 }" name="password">
                      <a-input-password
                        size="large"
                        type="password"
                        placeholder="请输入密码"
                      >
                        <template #prefix>
                          <LockOutlined style="color:rgba(0,0,0,.25)"
                        /></template>
                      </a-input-password>
                    </a-form-item>
                  </a-tab-pane>
                  <!-- 账号密码登陆结束 -->
                  <!-- 手机号登陆开始 -->
                  <a-tab-pane key="2" tab="手机号登陆">
                    Content of Tab Pane 2
                  </a-tab-pane>
                  <!-- 手机号登陆结束 -->
                </a-tabs>
              </a-col>
            </a-row>
            <!-- 登陆方式结束 -->
            <a-row>
              <a-col :span="24">
                <a-checkbox style="float:left">自动登陆</a-checkbox>
                <router-link to="#" style="float:right">忘记密码</router-link>
              </a-col>
            </a-row>
          </a-form>
          <!-- 表单结束 -->
          <a-row>
            <a-col :span="24">
              <span>其他登陆方式</span>
              <AlipayCircleOutlined class="item-icon" />
              <TaobaoCircleOutlined class="item-icon" />
              <WeiboCircleOutlined class="item-icon" />
              <router-link to="#" style="float: right">注册账户</router-link>
            </a-col>
          </a-row>
        </a-col>
      </a-row>
    </a-layout-content>
    <a-layout-footer></a-layout-footer>
  </a-layout>
</template>

<script>
import { UserOutlined, LockOutlined } from "@ant-design/icons-vue";
export default {
  components: {
    UserOutlined,
    LockOutlined,
  },
};
</script>

<style scoped>
.ant-layout {
  height: 100%;
  background-image: url(../assets/image/bg.svg);
}
.ant-layout-header {
  background-color: transparent;
}
.ant-form {
  width: 365px;
  margin: 0 auto;
}
.login-title {
  text-align: center;
}
.login-title h2 {
  position: relative;
  top: 2px;
  font-size: 33px;
  color: rgba(0, 0, 0, 0.85);
  font-family: Avenir, Helvetica Neue, Arial, Helvetica, sans-serif;
  font-weight: 600;
}
.login-title img {
  height: 44px;
}

.login-title span {
  font-size: 14px;
  color: rgba(0, 0, 0, 0.45);
  margin-top: 12px;
}
.item-icon {
  font-size: 24px;
  color: rgba(0, 0, 0, 0.2);
  position: relative;
  top: 4px;
  margin: 0 5px;
}

.item-icon:hover {
  color: #1890ff;
}
</style>
