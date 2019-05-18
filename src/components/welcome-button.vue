<template>
  <!--<button @click="$emit('welcome')">-->
  <!--Click me to be welcomed-->
  <!--</button>-->
  <input @change='childfun' type='text' v-model="v">

</template>

<script>
  export default {
    name: "welcome-button",
    props:['aaa'],
    data(){
      return{
        v:''
      }
    },
    methods: {
      childfun() {
        this.$emit('changes',this.v);//触发事件
      }
    }
  }
</script>

<style scoped>

</style>
