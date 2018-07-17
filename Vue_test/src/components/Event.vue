<template>
   <div>
     <ul>
        <li v-on:click.once="getItemInfo(index,$event)" v-for="(name,index) in names">{{name}}</li>
     </ul>
     <input type="text" @keyup.enter="getKeyInfo">
     <button v-on:click="pushArr">push me</button>
     <button v-on:click="getOdd">button</button>
     <p>{{msgRe}}</p>
   </div>
  
</template>
<script>
   export default{
       //data 
       data(){
           return{
               names:['iwen','wen','en'],
               nums:[1,2,3,4,5,6,7],
               message:"hello",
           }
         },
           methods:{
               getItemInfo(data,event){
                    console.log(data);
               },
               getKeyInfo(event){
                     console.log(event);  
               },
               pushArr(){
                   this.names.push("frank");
               },
               getOdd(){
                   this.nums.filter(function(num){
                       if(num%2==0)
                       console.log(num);
                   })
               }
           },
           computed:{
               msgRe(){
                   return this.message.split('').reverse().join('');
               }
           }
       }
</script>
<style>
</style>