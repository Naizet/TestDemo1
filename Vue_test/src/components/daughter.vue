<template>
   <div>
       女儿:{{title}}--{{lifemsg}}--{{num *2}}
   </div>
</template>
<script>
 export default{
     name:"daughter",
     data(){
         return {

         }
     },
     props:{
         title:[String,Number],
         lifemsg:String,
         num:Number
     }
 }
</script>
<style>
</style>