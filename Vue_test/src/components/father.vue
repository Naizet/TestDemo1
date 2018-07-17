<template>
    <div>
      父亲
      <input type="text" v-model="lifemsg">
      <daughter :title="msg" :lifemsg="lifemsg" :num="num"/>
      <button @click="changeMsg">click</button>
      
    </div>
</template>
<script>
import daughter from "./daughter"
export default {
    name:"father",
    data(){
        return{
            msg:"我是活的数据",
            lifemsg:"life",
            num:"10",
        }
    },
    components:{
        daughter,
    },
    methods:{
        changeMsg(event){
            this.msg="我是修改后的数据";
        }
    }

}
</script>
<style>

</style>
