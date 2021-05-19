<template>
    <div class="header">
        <h2 style="white-space:pre-line">{{message}}</h2>
        <textarea type="text" v-model="message" />
    </div>
</template>

<script>
export default {
    name:'main',
    data(){
        return{
            message:'Hello Vue I am ))))',

        }
    }
}
</script>