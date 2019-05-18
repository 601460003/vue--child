<template>
  <div class="hello">
    <div id="emit-example-simple">
      <apple ref="oppo" ></apple>
      <welcome-button  @changes="doSomeTing" :aaa='111' :bbb='222' ></welcome-button>
    </div>
    <h1 @click="home">{{ msg }}</h1>
    <dos></dos>
  </div>
</template>

<script>
  import dos from '@/components/dos.vue'
  import apple from '@/components/apple.vue'
  import welcomeButton from '@/components/welcome-button.vue'

  export default {
    name: 'HelloWorld',
    components: {
      dos, welcomeButton,apple
    },
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        aaa: 111,
        bbb: 222,
        ai:[]
      }
    },

    methods: {
      home() {
    this.ai=this.$refs.oppo.list
        console.log(this.ai)
      },
      sayHi() {
        alert('Hi2!')
      },
      doSomeTing: function (msg) {
        console.log(msg)
      },
      apple(o){
        alert(11)
      }
    }


  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
