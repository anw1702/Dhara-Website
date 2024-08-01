<script lang="ts">
	import DFTCard from './DFTCard.svelte';

	import Heart from '@/img/heart.svelte';
	import Trophy from '@/img/trophy.svelte';
	import Checkbox from '@/img/checkbox.svelte';
	import Rocket from '@/img/rocket.svelte';
	import Graph from '@/img/graph.svelte';
	import ArrowSec from '@/img/arrowsec.svelte';

	import DftMobile from '@/img/DFTMobile.svelte';
	import DftShort from '@/img/DFTShort.svelte';
	import Dftl1 from '@/img/DFTL1.svelte';
	import Dftl2 from '@/img/DFTL2.svelte';
	import Dftl3 from '@/img/DFTL3.svelte';

	const content = [
		{
			heading: 'Innovative Financing Solutions',
			body: '	DFT lets banks offer blockchain-based financing to SMEs, providing a flexible alternative to traditional credit lines.'
		},
		{
			heading: '	Enhanced Risk Management',
			body: "DFT's transparent ledger and smart contracts enhance banks' risk 	management, ensuring security with clear visibility and immutable records."
		},
		{
			heading: '		Expanding Clientele Base',
			body: 'DFT adoption helps banks attract new clients, especially underserved SMEs, expanding market share and revenue streams.'
		},
		{
			heading: '	Enhancing Client Relationships',
			body: 'DFT solutions help banks strengthen relationships with clients by offering advanced tools for effective supply chainfinancing management.'
		},
		{
			heading: 'Competitive Edge in Fintech',
			body: `Banks integrating DFT position themselves as fintech innovators,enhancing their brand as leaders in technology adoption`
		},
		{
			heading: '	Compliance Efficiency',
			body: `DFT's compliance tools aid banks in meeting regulations efficiently,simplifying reporting and audits with automated transaction recording.`
		}
	];
</script>

<section class="relative mb-36 mt-56 flex flex-col px-5 md:flex-row">
	<div class="relative mx-auto my-auto flex flex-col text-center md:mx-0 md:max-w-sm md:text-left">
		<h3
			class="text-4xl font-medium leading-10 text-zinc-800 dark:text-white max-md:max-w-full md:text-3xl"
		>
			Unlocking New <br />
			Opportunities with DFT
		</h3>
		<p
			class="mt-5 text-lg font-light leading-7 text-neutral-500 dark:text-gray-300 max-md:max-w-full md:text-base"
		>
			Deep Financing Tokens (DFT) could revolutionize supply chain finance for banks, expanding
			services, reaching new clients, and driving fintech innovation.
		</p>
	</div>
	<!-- Desktop View -->
	<span class="relative -bottom-40 -left-8 hidden h-[30vw] md:block">
		<Dftl1 />
	</span>
	<section class="relative flex">
		<div class="flex flex-col">
			<span class="relative left-[12vw] -z-10 hidden md:block">
				<Dftl2 />
			</span>
			<div class="hidden flex-col space-y-2 md:flex">
				{#each content.slice(0, 3) as { heading, body }, i}
					<DFTCard>
						<svelte:fragment slot="icon">
							{#if i == 0}
								<Rocket />
							{:else if i == 1}
								<Graph />
							{:else if i == 2}
								<ArrowSec />
							{/if}
						</svelte:fragment>
						<h3 slot="heading">{heading}</h3>
						<p slot="body">
							{body}
						</p>
					</DFTCard>
				{/each}
			</div>
			<span class="relative bottom-20 left-[20vw] -z-10 hidden md:block">
				<Dftl3 />
			</span>
		</div>

		<div class="relative bottom-28 ml-5 hidden flex-col space-y-2 md:flex">
			{#each content.slice(3, content.length) as { heading, body }, i}
				<DFTCard>
					<svelte:fragment slot="icon">
						{#if i == 0}
							<Heart />
						{:else if i == 1}
							<Trophy />
						{:else if i == 2}
							<Checkbox />
						{/if}
					</svelte:fragment>
					<h3 slot="heading">{heading}</h3>
					<p slot="body">
						{body}
					</p>
				</DFTCard>
			{/each}
		</div>
	</section>
	<!-- End of Desktop View -->

	<!-- Mobile Section -->
	<div class="mt-10 flex flex-col md:hidden">
		<span class="mx-auto flex items-center justify-center">
			<DftMobile />
		</span>
		{#each content as { heading, body }, i}
			<DFTCard>
				<svelte:fragment slot="icon">
					{#if i == 0}
						<Rocket />
					{:else if i == 1}
						<Graph />
					{:else if i == 2}
						<ArrowSec />
					{:else if i == 3}
						<Heart />
					{:else if i == 4}
						<Trophy />
					{:else if i == 5}
						<Checkbox />
					{/if}
				</svelte:fragment>
				<h3 slot="heading">{heading}</h3>
				<p slot="body">
					{body}
				</p>
			</DFTCard>
			{#if i != content.length - 1}
				<span class="mx-auto flex items-center justify-center">
					<DftShort />
				</span>
			{/if}
		{/each}
	</div>
	<!-- Mobile Section -->
</section>
