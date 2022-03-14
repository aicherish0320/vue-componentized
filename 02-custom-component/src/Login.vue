<template>
  <el-form class="form" ref="form" :model="user" :rules="rules">
    <el-form-item label="用户名" prop="username">
      <el-input v-model="user.username"></el-input>
    </el-form-item>
    <el-form-item label="密码" prop="password">
      <el-input type="password" v-model="user.password"></el-input>
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="login()">登录</el-button>
    </el-form-item>
  </el-form>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      user: {
        username: '',
        password: ''
      },
      rules: {
        username: [
          {
            required: true,
            message: '请输入用户名'
          }
        ],
        password: [
          {
            required: true,
            message: '请输入密码'
          }
        ]
      }
    }
  },
  methods: {
    login() {
      this.$refs.form.validate((valid) => {
        if (valid) {
          alert('success')
        } else {
          alert('failure')
          return false
        }
      })
    }
  }
}
</script>

<style scoped></style>
