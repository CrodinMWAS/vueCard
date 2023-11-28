<template>
    <form @submit.prevent="handleSubmit">
        <label>Cardholder Name</label>
        <input type="text" placeholder="e.g. Jane Appleseed" v-model="name">

        <label>Card Number</label>
        <input type="text" placeholder="e.g. 123456789" v-model="cardNum">

        <div id="date">
            <label>Exp. Date (MM/YY)</label>
            <input type="number" placeholder="MM" v-model="dateMonth">
            <input type="number" placeholder="YY" v-model="dateYear">
            
            <label>CVC</label>
            <input type="number" placeholder="e.g. 123" v-model="cvc">

            <button>Confirm</button>
        </div>
    </form>
</template>
<script>
export default {
    data(){
        return {
            name: '',
            cardNum: '',
            dateMonth: '',
            dateYear: '',
            cvc: ''
        }
    },
    methods:{
        handleSubmit(){
            this.$emit("dataTransfer",[this.name, this.cardNum, this.dateMonth, this.dateYear, this.cvc])
        }
    }
}
</script>
<style>
    
</style>