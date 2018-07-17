<template>
    <div>
        父组件
         <Child>
             <div slot="s1">
                 <p >插入的内容1</p>
                 <p >插入的内容11</p>
                 </div>                       
             <p slot-scope="props">
                 {{props.text}}
             </p>
        </Child>
    </div>
</template>
<script>
import Child from "./childSlot"
export default {
    name:"parents",
    data(){
        return{

        }
    },
    components:{
        Child,
    }
}
</script>
<style>
p{
    color: red;
}
</style>
