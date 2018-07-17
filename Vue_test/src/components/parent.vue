<template>
    <div>
        parent
        <child @sending="getMsg"/>
        {{info}}
    </div>
</template>
<script>
import child from "./child"
export default {
    name:"parent",
    data(){
        return{
            info:"",
        }
    },
    components:{
        child,
    },
    methods:{
        getMsg(data){
          this.info=data;
        }
    }
}
</script>
<style>

</style>
