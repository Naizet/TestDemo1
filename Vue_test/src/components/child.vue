<template>
    <div>
        
        <button @click="sending">convert</button>
    </div>
</template>
<script>
export default {
    name:"child",
    data(){
       return{
        msg:"子组件数据"
       }
    },
    methods:{
        sending(event){
            //两个参数，key  数据
          this.$emit("sending",this.msg);
        }
    }
}
</script>
<style>

</style>
