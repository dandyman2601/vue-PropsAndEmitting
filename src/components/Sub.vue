<template>

    <div>
        <input type="button" name="button" value="-" @click="subtraction()"/>        
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
        subtraction(){
            let result = parseInt(this.getInput1) - parseInt(this.getInput2)                 
            this.$emit('getSubResult', result)                
        }
    }
}
</script>

<style>

</style>