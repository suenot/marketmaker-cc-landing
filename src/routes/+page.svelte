<script>
	import { onMount } from 'svelte';
	
	let isVisible = false;
	
	onMount(() => {
		isVisible = true;
	});
</script>

<svelte:head>
	<title>Marketmaker.cc - Next-Gen Trading Platform</title>
	<meta name="description" content="Advanced trading terminal, portfolio management, and strategy builder platform" />
</svelte:head>

<div class="min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 text-white">
	<!-- Hero Section -->
	<section class="py-20 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
		<div class="text-center">
			<h1 class="text-5xl md:text-6xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-emerald-400">
				Marketmaker.cc
			</h1>
			<p class="text-xl md:text-2xl text-gray-300 mb-8">
				Next-Generation Trading Platform for Professional Traders
			</p>
			<div class="flex justify-center gap-4">
				<a href="#contact" class="bg-blue-500 hover:bg-blue-600 px-8 py-3 rounded-lg font-semibold transition-colors">
					Contact Us
				</a>
				<a href="#roadmap" class="border border-blue-500 hover:bg-blue-500/10 px-8 py-3 rounded-lg font-semibold transition-colors">
					View Roadmap
				</a>
			</div>
		</div>
	</section>

	<!-- Key Features -->
	<section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto" id="features">
		<h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Platform Features</h2>
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
			{#each [
				{
					title: 'Trading Terminal',
					description: 'Real-time data providers, unified interface for all exchanges, and advanced order management',
					icon: '💻'
				},
				{
					title: 'Portfolio Management',
					description: 'Portfolio tree management, rebalancing, and virtual portfolios with tokens',
					icon: '💼'
				},
				{
					title: 'Historical Data',
					description: 'Ready-to-use API providers and custom data collection in Clickhouse/DuckDB',
					icon: '📅'
				},
				{
					title: 'Strategy Builder',
					description: 'Visual bot constructor, 100+ strategies, and integration with TradingView',
					icon: '🤖'
				},
				{
					title: 'Strategy Testing',
					description: 'Comprehensive testing on historical data, virtual portfolios, and real accounts',
					icon: '🧪'
				},
				{
					title: 'Analytics',
					description: 'Advanced market analysis, signals, and automated trading solutions',
					icon: '📊'
				}
			] as feature}
			<div class="bg-gray-800/50 p-6 rounded-xl hover:bg-gray-800/70 transition-colors">
				<div class="text-4xl mb-4">{feature.icon}</div>
				<h3 class="text-xl font-semibold mb-2">{feature.title}</h3>
				<p class="text-gray-400">{feature.description}</p>
			</div>
			{/each}
		</div>
	</section>

	<!-- Roadmap -->
	<section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto" id="roadmap">
		<h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Development Roadmap</h2>
		<div class="space-y-8">
			{#each [
				{
					stage: 'PRE-SEED STAGE 1',
					title: 'Trading Terminal',
					features: [
						'Real-time data providers',
						'Trading order management',
						'Unified exchange interface',
						'Payment processing'
					]
				},
				{
					stage: 'PRE-SEED STAGE 2',
					title: 'Portfolio Management',
					features: [
						'Portfolio tree management',
						'Portfolio rebalancing',
						'Accounting visualization',
						'Virtual portfolios and tokens',
						'First sales MVP'
					]
				},
				{
					stage: 'SEED STAGE 1',
					title: 'Strategy Builder',
					features: [
						'Visual bot constructor',
						'Building block creation',
						'100+ strategy implementation',
						'TradingView integration',
						'GitHub strategy collection'
					]
				}
			] as phase}
			<div class="bg-gray-800/30 rounded-xl p-6 hover:bg-gray-800/50 transition-colors">
				<div class="flex items-center justify-between mb-4">
					<h3 class="text-xl font-semibold text-blue-400">{phase.stage}</h3>
					<span class="px-3 py-1 bg-blue-500/20 rounded-full text-blue-300 text-sm">{phase.title}</span>
				</div>
				<ul class="space-y-2">
					{#each phase.features as feature}
						<li class="flex items-center">
							<span class="mr-2">•</span>
							{feature}
						</li>
					{/each}
					
				</ul>
			</div>
			{/each}
			
		</div>
	</section>

	<!-- Team -->
	<section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto" id="team">
		<h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Our Team</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each [
				{ name: '@suenot', role: 'Chief Executive Officer', skills: 'Fullstack, DevOps' },
				{ name: '@ibnteo', role: 'Chief Technology Officer', skills: 'Fullstack' },
				{ name: '@aliex_z', role: 'Chief Financial Officer', skills: 'Fullstack' },
				{ name: '@timax', role: 'Head of Quantitative Research', skills: 'Fullstack' },
				{ name: '@thatmean', role: 'Risk Manager', skills: 'Fullstack' },
				{ name: '@markinmatrix', role: 'Business Development Manager', skills: 'Fullstack' },
				{ name: '@alexlog', role: 'Quant Researcher', skills: '' },
				{ name: '@your_name', role: 'Be Part of Our Team', skills: '' }
			] as member}
			<div class="bg-gray-800/30 p-6 rounded-xl text-center hover:bg-gray-800/50 transition-colors">
				<div class="w-20 h-20 bg-gray-700 rounded-full mx-auto mb-4"></div>
				<h3 class="text-lg font-semibold mb-1">{member.name}</h3>
				<p class="text-blue-400 text-sm mb-2">{member.role}</p>
				{#if member.skills}
					<p class="text-gray-400 text-sm">{member.skills}</p>
				{/if}
				
			</div>
			{/each}
			
		</div>
	</section>

	<!-- Tech Stack -->
	<section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
		<h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Technology Stack</h2>
		<div class="flex flex-wrap justify-center gap-4">
			{#each ['Golang', 'Rust', 'Python', 'TypeScript', 'Elixir', 'ClickHouse', 'DuckDB', 'PostgreSQL', 'Hasura', 'GraphQL', 'gRPC'] as tech}
				<span class="px-4 py-2 bg-gray-800/50 rounded-lg text-gray-300">{tech}</span>
			{/each}
			
		</div>
	</section>

	<!-- Investment Section -->
	<section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto bg-blue-500/10 rounded-xl" id="contact">
		<div class="text-center max-w-3xl mx-auto">
			<h2 class="text-3xl md:text-4xl font-bold mb-6">Investment Opportunity</h2>
			<p class="text-xl mb-8">
				Valuation: $10M USDT<br>
				Pre-seed round: 5% for $500k USDT<br>
				<span class="text-gray-400">(Valuation as of January 2025)</span>
			</p>
			<div class="bg-gray-800/50 p-8 rounded-xl">
				<h3 class="text-2xl font-semibold mb-4">Connect With Us</h3>
				<p class="text-gray-300 mb-6">
					Ready to be part of the next generation of trading technology? Contact us to discuss investment opportunities.
				</p>
				<a
					href="mailto:contact@marketmaker.cc"
					class="inline-block bg-blue-500 hover:bg-blue-600 px-8 py-3 rounded-lg font-semibold transition-colors"
				>
					Contact for Investment
				</a>
			</div>
		</div>
	</section>
</div>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}
</style>