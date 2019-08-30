<template>
	<div class="row">
		<div class="col-sm-12">
			<h3>Add Quotes</h3>
          <div class="progres">
	      <div class="progress">
		  <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
           :style="{width:(quotescount/maxquotes)* 100 + '%'}"
		  >

		  {{quotescount}}/{{maxquotes}}

		  </div>
	</div>
</div>
		</div>
	</div>

</template>

<script>
	
export default {
        
   props:['quotescount','maxquotes']
       
    }

</script>
<style>
	

</style>