<template>
  <Card :number="number" :name="name" :expDateM="expDateM" :expDateY="expDateY" :cvc="cvc"></Card>
  <div id="gradient"></div>
  <Input @dataTransfer="fillCard"></Input>
</template>

<script>
import Input from './components/Input.vue'
import Card from './components/Card.vue'


export default {
  components:{ Input, Card },
  data(){
    return{
      number: "",
      name: "",
      expDateM: "",
      expDateY: "",
      cvc: ""
    }
  },
  methods:{
    fillCard(array){
      console.log(array)
      this.number = array[1]
      this.name = array[0]
      this.expDateM = array[2]
      this.expDateY = array[3]
      this.cvc = array[4]
    }
  }
  }
  
</script>


<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
