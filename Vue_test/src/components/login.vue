<template>
    <div>
       <input type="text" v-model.number="msg">
       <p>{{message}}</p>
    </div>
</template>
<script>
 export default{
     data(){
         return{
             msg:"hhh",
             message:"hhh",
         }
     },
     watch:{
       msg:function(data){
            setTimeout(() =>{
                this.message=data;
            },1000)
        }
     }
 }
</script>
<style>

</style>