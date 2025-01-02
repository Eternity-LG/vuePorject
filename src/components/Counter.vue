<template>
  <div class="counter">
    <input type="text" v-model="count" readonly />
    <button @click="increment">Count +2</button>
  </div>
</template>

<script>
export default {
  name: 'NumberCounter', // 组件名称，使用多词组合以符合Vue规范
  data() {
    return {
      count: 0 // 计数器的初始值
    }
  },
  methods: {
    increment() {
      this.count += 2 // 每次点击增加2
    }
  }
}
</script>

<style scoped>
/* 计数器容器样式 */
.counter {
  margin: 20px;
  display: flex;
  gap: 10px;
  justify-content: center;
}

/* 输入框样式 */
input {
  padding: 5px;
  width: 60px;
  text-align: center;
}

/* 按钮样式 */
button {
  padding: 5px 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

/* 按钮悬停效果 */
button:hover {
  background-color: #45a049;
}
</style>
