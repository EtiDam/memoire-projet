<script>
  import BarChart from '@onsvisual/svelte-charts/src/charts/BarChart.svelte';
import { themes } from '../config.js';
	import { getContext } from 'svelte';

	export let theme = getContext('theme');
	export let filled = false;
	export let center = true;
</script>

<nav style="border-bottom-color: {themes[theme]['muted']}; {filled ? 'background-color: ' +  themes[theme]['background'] + ';' : ''}">
  <div class="col-wide middle" class:center>
		<a href="https://uclouvain.be/fr/index.html">
			<picture>
				{#if theme == 'dark'}
				<img src="./img/ons-logo-black-en.svg" alt="UCLouvain">
				{:else if filled == true}
				<img src="./img/ons-logo-black-en.svg" alt="UCLouvain">
				{:else}
				<img src="./img/ons-logo-black-en.svg" alt="UCLouvain">
				{/if}
			</picture>
		</a>
  </div>
</nav>

<style>
	nav {
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		position: relative;
		height: 46px;
		margin-bottom: -46px;
		border-bottom: 1px solid #777;
		z-index: 1;
	}
	picture {
		position: relative;
		top: -3px;
		padding: 0 5px;
	}
	picture2 {
		position: relative;
		top: -3px;
		padding: 0 5px;
	}
	img {
		width: 270px;
	}
	a img:hover {
		cursor: pointer;
	}
</style>