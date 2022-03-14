<template>
  <ac-form class="form" ref="form" :model="user" :rules="rules">
    <ac-form-item label="用户名" prop="username">
      <ac-input v-model="user.username" placeholder="请输入用户名"></ac-input>
    </ac-form-item>
    <ac-form-item label="密码" prop="password">
      <ac-input
        type="password"
        v-model="user.password"
        placeholder="请输入密码"
      ></ac-input>
    </ac-form-item>
    <ac-form-item>
      <ac-button type="primary" @click="login()">登录</ac-button>
    </ac-form-item>
  </ac-form>
</template>

<script>
import AcForm from './form/Form.vue'
import AcFormItem from './form/FormItem.vue'
import AcInput from './form/Input.vue'
import AcButton from './form/Button.vue'
export default {
  name: 'FormTest',
  components: {
    AcForm,
    AcFormItem,
    AcInput,
    AcButton
  },
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
      // this.$refs.form.validate((valid) => {
      //   if (valid) {
      //     alert('success')
      //   } else {
      //     alert('failure')
      //     return false
      //   }
      // })
      console.log('button')
    }
  }
}
</script>

<style scoped></style>
