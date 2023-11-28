<template>
    <div id="card" v-if="expDateM">
        <div id="circles">
            <div id="circle"></div>
            <div id="hollowCircle"></div>
        </div>
        <h1>{{ number }}</h1>
        <div id="card-data">
            <h3 id="name">{{ name }}</h3>
            <h3 id="expDate">{{ expDateM }} / {{ expDateY }}</h3>
        </div>
    </div>
    <div id="backOfCard">
        <div id="line">
            <h5 id="cvc">{{ cvc }}</h5>
        </div>
    </div>
</template>
<script>
export default {
    props: ["number", "name", "expDateM", "expDateY", "cvc"]
}
</script>
<style scoped>
    #circles{
        display: flex;
        align-items: center;
    }
    #circle{
        border-radius: 50%;
        width: 50px;
        height: 50px;
        background-color: white;
        margin-right: 15px;
    }
    #hollowCircle{
        border-radius: 50%;
        width: 25px;
        height: 25px;
        outline: 2px solid white;
    }
    #card{
        background-color: green;
        width: 400px;
        margin: auto;
        border-radius: 5px;
        padding: 20px;
        color: white;
    }
    #card-data{
        display: flex;
        justify-content: space-around;
    }
</style>