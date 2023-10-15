<template>

	<div class="container">
		

		<p>
			{{msg}}
		</p>
		
	</div>
</template>

<script>
	export default {
		name: 'Inicial',
		props: {
			msg: String
		},
		data: function () {
			return {
				name:'Nome',
			}
		},
		methods:{
			greet: function metodo01(params) {
				return `Frase ${params} .`; 
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
	.container{
		p{
			color: blue;
		}
	}
</style>
