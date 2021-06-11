<template>

    <div>
        <input type="button" name="button" value="+" @click="addition()"/>        
    </div>

</template>

<script>
export default {
    props: ['getInput1', 'getInput2'],

    data(){
        return{
            
        }
    },
    methods: {
        addition(){
            let result = parseInt(this.getInput1) + parseInt(this.getInput2)                 
            this.$emit('getAddResult', result)
            console.log(this.getInput1 + ' AND ' + this.getInput2)    
        }
    }
}
</script>

<style>
div{
    display: inline-block;
}
</style>