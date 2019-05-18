<template>
    <button @click="oo">app</button>
</template>

<script>
    export default {
        name: "apple",
      data(){
        return{
          list:[{name:'xiaoming',age:19}]
        }
      },

      methods:{
          ok(){
            // this.$emit('oppo',this.list[0].name)
            alert('aaaaa')
          },
        oo(){

          // this.$emit('ttt',121)

          this.$emit('oppo',this.list[0].name)

        }
      }
    }
</script>

<style scoped>

</style>
