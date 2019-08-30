<template>
    <div class="row">
    	<app-quotes v-for="(quote,index) in quotes" @click.native="deletequotes(index)">{{quote}}</app-quotes>
    </div>
</template>

<script>
	import Quotes from './Quotes.vue';
    export default {
        

        props:['quotes'],
        components:{
        	appQuotes:Quotes,
        },
        methods:{
        	deletequotes(index){
              this.$emit('quotesdeleted',index);
        	}
        }
    }
</script>

<style>

</style>
