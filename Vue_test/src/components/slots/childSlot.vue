<template>
    <div>
         子组件
         <slot name="s1">
         </slot>
         <hr />
         <slot name="s2">
           <p>  如果没有插入内容，则显示无</p>
         </slot>
          <slot text="我是数据传递"></slot>
    </div>
</template>

<script>
export default {
    name:"Child",
    data(){
        return{

        }
    }
}
</script>
