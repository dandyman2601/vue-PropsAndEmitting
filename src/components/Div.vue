<template>

    <div>
        <input type="button" name="button" value="/" @click="division()"/>        
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
        division(){
            let result = parseInt(this.getInput1) / parseInt(this.getInput2)                 
            this.$emit('getDivResult', result)
        }
    }
}
</script>

<style>

</style>