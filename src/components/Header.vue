<template>
<header>
	<div class="navbar navbar-default">
		<div class="navbar-header">
			<h1>
				<router-link :to="{name:'iMain'}">
					{{sitename}}
				</router-link>
			</h1>
		</div>
		<div class="nav navbar-nav navbar-right cart">
			<button type="button" class="btn btn-default btn-lg" @click="showCheckout">
				<span class="glyphicon glyphicon-shopping-cart">{{ cartItemCount }} </span> Checkout
			</button>
		</div>
	</div>
</header>
</template>

<script>
export default {
	name: 'hello',
	data () {
		return {
			sitename: 'Pet Depot'
		}
	},
	props: ['cartItemCount'],
	methods: {
		showCheckout () {
			this.$router.push({name: 'Form'})
		}
	}
}
</script>

<style scoped>

</style>
