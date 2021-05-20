<template>
    <div class="header">
        <h2 style="white-space:pre-line">{{message}}</h2>
        <div class="section">
        <div class="texts">
        <textarea type="text" v-model="message" />
        </div>
        
        <button v-on:click="clear">Clear</button>
        <button v-on:click="makeCaptial">Cap</button>
        </div>
    
    </div>
</template>

<script>
export default {
    name:'main',
    data(){
        return{
            message:'Hello Vue I am ))))',

        }
    },
    methods:{
        clear: function(){
            this.message= "";
        },
        makeCaptial: function(){
            this.message = this.message.toUpperCase();
        }
    }
};
</script>

<style>
.section{
    display: flex;
    justify-content: center;
    align-items: center;
}
button{
    margin-top: -3px;
    padding-left: 10px;
    padding-top: 12px;
    padding-right: 10px;
    padding-bottom: 6px;
}
</style>