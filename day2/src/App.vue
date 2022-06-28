<template>
  <!-- 目标: 点击按钮 - 把文字取反显示 - 再点击取反显示(回来了) -->
  <!-- <div>
    <h1>{{msg}}</h1>
    <button @click="reverse">逆转世界</button>
  </div> -->

    <!-- 需求点：

  1. 完成页面初搭
  2. 选择所在地区有默认选中 中国大陆
  3. 年龄 只可以 输入数字
  4. 爱好 默认选中 学习 写代码 这两项
  5. 信息展示部分 爱好 展示 以逗号 做为分割符
  6. 信息展示部分 是否记住密码 用是和否 -->

  <div>
    <div>
      <span>选择所在地区：</span>
      <input type="radio" value="中国大陆" name="area" v-model="area">中国大陆
      <input type="radio" value="中国香港" name="area" v-model="area">中国香港
    </div>
    <div>
      <span>手机号码：</span>
      <input type="text" name="phone" v-model="phone">
    </div>
    <div>
      <span>年龄: </span>
      <input type="text" name="age" v-model="age">
    </div>
    <div>
      <span>密码：</span>
      <input type="password" name="password" v-model="password">
    </div>
    <div>
      <span>爱好：</span>
      <input type="checkbox" v-model="hobby" value="看书">看书
      <input type="checkbox" v-model="hobby" value="学习">学习
      <input type="checkbox" v-model="hobby" value="写代码">写代码
      <input type="checkbox" v-model="hobby" value="游戏">游戏
    </div>
    <div>
      <input type="checkbox" v-model="isgrow"> 记住密码
    </div>
    <div>====================================================</div>
    <div>
      我来自：{{area}}
      <br>
      手机号码是：{{phone}}
      <br>
      年龄是：{{age}}
      <br>
      密码是：{{password}}
      <br>
      爱好是：{{hobby.join('&')}}
      <br>
      是否记住密码：{{isgrow ? '是' : '否'}}
    </div>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    // return {
    //   msg: 'Hello, World',
    // }
    return {
      area: '中国大陆',
      phone: '',
      age: '',
      password: '',
      hobby: ['学习','写代码'],
      isgrow: true,
    }
  },
  methods: {
    // reverse() {
    //   this.msg = this.msg.split('').reverse().join('')
    // },
  },
}
</script>

<style></style>
