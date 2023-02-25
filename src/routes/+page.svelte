<svelte:head>
	<title>Expenses chart component</title>
</svelte:head>

<main class="bg-cream w-screen h-screen flex justify-center items-center font-dm-sans">
	<div class="flex flex-col w-[500px] gap-6">
		<div class="flex bg-soft-red rounded-2xl p-6 justify-between">
			<div class="text-white">
				<p class="mb-2">My balance</p>
				<h2 class="text-3xl font-bold">$921.48</h2>
			</div>
			<img src="/images/logo.svg" alt="">
		</div>
		<div class="bg-very-pale-orange rounded-2xl p-6">
			<h1 class="text-3xl font-bold text-dark-brown">Spending - Last 7 days</h1>
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