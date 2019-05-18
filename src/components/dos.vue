<template>
    <div>
      <button >添加</button>
    </div>
</template>

<script>
    export default {
      data(){
        return{
          list:[{name:'xiaoming',age:19}]
        }
      },
        methods:{
          add(){
            console.log(11)
          }
        }
    }
</script>

<style scoped>
body{

}
</style>
