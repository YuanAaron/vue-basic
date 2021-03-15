<template>
  <!-- <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div> -->
  <div id=app>
        {{msg}}
        <div>
            <input type="text" v-model="info">
            <button v-on:click="handlerClick">添加</button>
            <ul>
                <todo-item v-for="item in list" :key="item">
                  <span slot="item" style="font-size: 20px">{{item}}</span>
                </todo-item>
            </ul>
        </div>
    </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

//TodoItem相当于App的一个子组件
import TodoItem from './components/TodoItem.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    TodoItem
  },
  data() {
      return {
          msg: "hello vue!",
          info: '',
          list: []
      }
  },
  methods: {
      handlerClick() {
          this.list.push(this.info);
          this.info='';
      }
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
