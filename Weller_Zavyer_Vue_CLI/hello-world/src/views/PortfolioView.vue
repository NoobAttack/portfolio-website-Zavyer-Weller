<template>
	<div class="portfolio-view">
		<Portfolio />
	</div>
</template>

<script>
import Portfolio from '../components/Portfolio.vue';

export default {
	name: 'PortfolioView',
	components: {
		Portfolio,
	},
};
</script>

<style scoped>
/* Component now handles its own styles */
.portfolio-view {
	padding-top: 20px;
}
</style>
