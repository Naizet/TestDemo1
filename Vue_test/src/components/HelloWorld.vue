<template>
  <div class="hello">
  {{msg }}
  {{ 1+1 }}
  {{0>10 ? '对的' :'错的'}}
  {{'注意：只能存在单行语句' }}
  <p>{{flag}}</p>
  <p v-html='hello'></p>
   <p v-text='hello'></p>
   <span v-bind:class ="ha">hahaha</span>
   {{ message.split('').reverse().join('') }}
   <a href="LoginForm">denglu</a>
   <div>
    <template v-if="show">我是if为true看到的</template>
    <template v-else>我是if为false看到的</template>
   </div>
   <div>
    <p v-show="show">qubie</p>
   </div>
   <div class="list">
      <ul>
         <li v-for="(name,index) in names" v-bind:key="index">{{name }}--{{index}}</li>
      </ul>
     
   </div>
   <button v-on:click="num+=1">click </button>
   <p>{{num}}</p>
   <button v-on:click="handler">按钮</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      num:1,
      msg: 'Welcome to Your Vue.js App',
      flag:'我是flag',
      hello:'<p>stupid</p>',
      ha:'ha1',
      message:'zhoujielun',
      show:true,
      names:['iwen','wen','en'],
    }
  },
  methods:{
    handler(){
      this.show=!this.show;
      alert("我是点击事件");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.ha{
  color:red;
}
</style>
