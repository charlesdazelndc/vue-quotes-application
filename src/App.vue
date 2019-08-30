<template>
    <div class="container">
    <app-header :quotescount="quotes.length" :maxquotes="maxquotes"></app-header>
    <app-newquotes  @newadded="qutesadded"></app-newquotes>
    <app-quotesdiv :quotes="quotes" @quotesdeleted="deletequote"> </app-quotesdiv>

    <div class="col-sm-12 text-center">
    	
       <div class="alert alert-info">Info:click on Delete quotes</div>
    </div>
    </div>
</template>

<script>

	import Quotesdiv from './components/Quotesdiv.vue';
	import Newquotes from './components/Newquotes.vue';
	import Header from './components/Header.vue';
    export default {
            data:function(){
        	return{

        		quotes:[

                  'this is sample Quotes'
        		],
        		maxquotes:10,
        	}
        },

        methods:{
          qutesadded(quote){
            this.quotes.push(quote);
          },
          deletequote(index){
          	this.quotes.splice(index,1);

          }

        },

        components:{
        	appQuotesdiv:Quotesdiv,
        	appNewquotes:Newquotes,
        	appHeader:Header,
        }

    }
</script>

<style>
</style>
