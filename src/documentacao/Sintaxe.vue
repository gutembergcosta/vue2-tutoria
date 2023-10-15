<template>

	<div class="container">

		<div class='row'>
			<div class='col-md-12 d-flex'>
				<div class="card my-5" style="width:300px" >
					<div class="card-body">
						<h3 class="card-title">Interpolações</h3>

						<h5>Texto</h5>
						<p>Mensagem: {{ msg }}</p>
						<p v-once>Esse valor nunca será modificado: {{ msg }}</p>
						
						<h5>Raw HTML</h5>
						<p>Interpolação textual: {{ rawHtml }}</p>
						<p>Diretiva v-html: <span v-html="rawHtml"></span></p>
						
						<h5>Atributos</h5>
						<p v-bind:id="dynamicId">dynamicId</p>

						<h5>Expressões javascript</h5>
						<p>{{ number + 1 }}</p>
						<p>{{ ok ? 'YES' : 'NO' }}</p>
						<p>{{ msg.split('').reverse().join('') }}</p>
						<p v-bind:id="'list-' + id">'list-' + id</p>	
							
					</div>
				</div>
				
				<div class="card m-5" style="width:300px" >
					<div class="card-body">
						<h3 class="card-title">Diretivas</h3>
						<p v-if="seen">Now you see me</p>							
						<h5>Arguments</h5>
						<a v-bind:href="url"> {{ url }} </a>

					</div>
				</div>
			</div>
		</div>		
		
	</div>
</template>

<script>
	export default {
		name: 'Sintaxe',
		
		data: function () {
			return {
				msg:'Texto',
				rawHtml:'<a>link</a>',
				dynamicId:'dynamic-id',
				number: 3,
				ok: true,
				id: 101,
				seen: true,
				url: 'http://localhost:8080/'
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
	
</style>
