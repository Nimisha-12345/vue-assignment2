<template>
    <div class="header">
        <h2 style="white-space:pre-line">{{message}}</h2>
        
        <textarea type="text" v-model="message" />
        
        <button v-on:click="clear">Clear</button>
        <button v-on:click="makeCaptial">Cap</button>
    
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