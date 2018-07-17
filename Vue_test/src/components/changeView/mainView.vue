<template>
    <div>
        主面板
        <keep-alive>
             {{current}}
        </keep-alive>
        <p><button @click="change">click</button></p>

        <button @click="viewchange">button</button>
        <transition name="fade">
            <p v-show="show">changeview</p>
        </transition>
        <!--现在index.html中引入 引入外部css文件 -->
        <button @click="anim">css文件引入</button>
        <transition
    name="custom-classes-transition"
    enter-active-class="animated tada"
    leave-active-class="animated bounceOutRight"
  >
    <p v-if="animShow">hello</p>
  </transition>
       <!-- 用svg画图形 -->
    <svg width="100%" height="100%" version="1.1"
        xmlns="http://www.w3.org/2000/svg">

        <rect width="300" height="100"
        style="fill:rgb(0,0,255);stroke-width:1;
        stroke:rgb(0,0,0)"/>
    </svg>

         
     <!-- 输入框获取焦点 -->
     <input v-focus type="text">
     <p v-mycss>disorder</p>
     <!-- 过滤器 -->
     <p>{{ price | money}}</p>
     <p>{{ context | contextDate}}</p>
     <p>{{ price | contextDate}}</p>
    </div>

</template>
<script>
import view1 from "./view1";
import view2 from "./view2";
export default {
  name: "Main",
  data() {
    return {
      current: "view1",
      flag: true,
      show: true,
      animShow: true,
      price: 20,
      context:"文本信息"
    };
  },
  components: {
    view1,
    view2
  },
  methods: {
    change() {
      if (this.flag) {
        this.current = "view1";
        this.flag = false;
      } else {
        this.current = "view2";
        this.flag = true;
      }
    },
    viewchange() {
      this.show = !this.show;
    },
    anim() {
      this.animShow = !this.animShow;
    }
  },
  //   局部变量
  directives: {
    focus: {
      // 指令的定义
      inserted: function(el) {
        el.focus();
      }
    },
    mycss: {
      inserted: function(el) {
        el.style.color = "red";
      }
    }
  },
  filters: {
      money(value){
         if(typeof value ==="number"){
             return "￥"+value;
         }
         return value;
      },
      contextDate(value){
          return value + new Date();
      }
  }
};
</script>
<style>
.fade-enter-active {
  opacity: 0.5s;
}
</style>
