<script lang="ts">
	import DFTCard from './DFTCard.svelte';

	import Heart from '@/img/heart.svelte';
	import Trophy from '@/img/trophy.svelte';
	import Checkbox from '@/img/checkbox.svelte';
	import Rocket from '@/img/rocket.svelte';
	import Graph from '@/img/graph.svelte';
	import ArrowSec from '@/img/arrowsec.svelte';
	import L1 from '@/img/line1.svelte';
	import Convo from '@/img/convo.svelte';
	import DftMobile from '@/img/DFTMobile.svelte';
	import DftShort from '@/img/DFTShort.svelte';

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

<section>
	<div class="overflow-hidden px-20 py-10 max-md:px-5">
		<div class="flex gap-5 max-md:flex-col">
			<div class="flex w-[36%] flex-col max-md:ml-0 max-md:w-full">
				<div class="my-auto flex flex-col self-stretch max-md:mt-10 max-md:max-w-full">
					<h3 class="text-4xl font-medium leading-10 text-zinc-800 max-md:max-w-full">
						Unlocking New <br />Opportunities with DFT
					</h3>
					<p class="mt-5 text-lg font-light leading-7 text-neutral-500 max-md:max-w-full">
						Deep Financing Tokens (DFT) could revolutionize supply chain finance for banks,
						expanding services, reaching new clients, and driving fintech innovation.
					</p>
				</div>
			</div>
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
		</div>
	</div>

	<div class="mx-auto flex items-center justify-center">
		<Convo />
	</div>
</section>
