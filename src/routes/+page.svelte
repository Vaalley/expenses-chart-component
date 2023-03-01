<script>
	import { onMount } from 'svelte';
	import data from '../../data.json';
	
	onMount(() => {
		console.log(data);
	})
</script>

<svelte:head>
	<title>Expenses chart component</title>
</svelte:head>

<main class="bg-cream w-screen h-screen flex justify-center items-center font-dm-sans">
	<div class="flex flex-col w-[500px] gap-6">
		<div class="flex bg-soft-red rounded-2xl p-8 justify-between">
			<div class="text-white">
				<p class="mb-2">My balance</p>
				<h2 class="text-3xl font-bold">$921.48</h2>
			</div>
			<img src="/images/logo.svg" alt="">
		</div>
		<div class="bg-very-pale-orange rounded-2xl p-8">
			<h1 class="text-3xl font-bold text-dark-brown mb-6">Spending - Last 7 days</h1>
			<div class="flex justify-between mb-2">
				{#each data as {day, amount}, i}
				<div class="w-11 -lg:w-8 h-20 bg-soft-red rounded-sm hover:bg-cyan hover:cursor-pointer"></div>
				{/each}
			</div>
			<div class="flex justify-between">
				{#each data as {day, amount}, i}
				<div class="w-11 -lg:w-8 flex justify-center">
					<p class="text-medium-brown text-sm">{day}</p>
				</div>
				{/each}
			</div>
			<hr class="my-6">
			<div class="flex justify-between items-end">
				<div>
					<p class="text-medium-brown mb-2">Total this month</p>
					<h2 class="text-dark-brown text-5xl font-bold">$478.33</h2>
				</div>
				<div class="text-right">
					<p class="font-bold text-dark-brown">+2.4%</p>
					<p class="text-medium-brown">from last month</p>
				</div>
			</div>
		</div>
	</div>
</main>