// 样式绑定

<template>
    
    <div>
    
          <p v-bind:class="{active:isactive}">haha</p>
          <p v-bind:class="styleObj">shazi</p>
          <p v-bind:class="[demo1,demo2]">stupid</p>
            <ul>
                <li v-bind:class="{active:index%2==0}" v-for="(name,index) in names">{{ name}}</li>
            </ul>
    
        <p :style="stob">hello world</p>
    
    </div>
    
</template>
<script>
export default {
  name: "style",
  data() {
    return {
      isactive: false,
      styleObj: {
        active: true
      },
      demo1: "demo1",
      demo2: "demo2",
      names: ["iwen", "wen", "en", "e"],
      stob: {
        color: "#ff8080"
      }
    };
  }
};
</script>
<style>
.active {
  color: red;
  background: #f1f1f1;
}
</style>

