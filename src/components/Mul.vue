<template>

    <div>
        <input type="button" name="button" value="x" @click="multiply()"/>        
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
        multiply(){
            let result = parseInt(this.getInput1)*parseInt(this.getInput2)               
            this.$emit('getMulResult', result)            
        }
    }
}
</script>

<style>

</style>