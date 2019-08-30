<template>



<form>

<div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-4 form-group">
<label>Quotes</label>
<textarea class="form-control" rows="3" v-model="quote"></textarea>
</div>



<div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-4 form-group">
<button class="btn btn-primary" @click.prevent="addnewquotes()">AddQuotes</button>
</div>

</form>


</template>

<script>
	
    export default {
        data:function()
        {
            return{
                quote:"",
            }
        },

        methods:{
                addnewquotes(){
                this.$emit('newadded',this.quote);
                this.quote="";

            }

        }

        
    }
</script>

<style>

</style>
