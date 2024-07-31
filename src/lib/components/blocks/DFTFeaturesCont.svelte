<script lang="ts">
	import { onMount } from 'svelte';
	import DFTCard from './DFTCard.svelte';

	import Heart from '@/img/heart.svelte';
	import Trophy from '@/img/trophy.svelte';
	import Checkbox from '@/img/checkbox.svelte';
	import Rocket from '@/img/rocket.svelte';
	import Graph from '@/img/graph.svelte';
	import ArrowSec from '@/img/arrowsec.svelte';
	import L1 from '@/img/line1.svelte';
	import Convo from '@/img/convo.svelte';
	import CountryCodeSelector from './CountryCodeSelector.svelte';

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

	interface ContactFormProps {
		onSubmit: (formData: FormData) => void;
	}

	export let onSubmit: ContactFormProps['onSubmit'];

	let fullName = '';
	let email = '';
	let phoneNumber = '';
	let message = '';
	let agreedToPolicy = false;

	function handleSubmit(event: Event) {
		event.preventDefault();
		const formData = new FormData();
		formData.append('fullName', fullName);
		formData.append('email', email);
		formData.append('phoneNumber', phoneNumber);
		formData.append('message', message);
		formData.append('agreedToPolicy', agreedToPolicy.toString());
		onSubmit(formData);
	}

	onMount(() => {
		const form = document.getElementById('contactForm');
		if (form) {
			form.setAttribute('novalidate', '');
		}
	});
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

	

	<div class="relative mx-auto flex items-center justify-center mb-5">

		<div class="absolute p-6 w-full md:w-[50%] mx-auto md:mx-0 md:mr-auto  md:left-[10%] md:top-[45%] md:transform md:translate-y-[-40%]">
			<h1 class="w-full text-5xl font-medium text-white leading-[58px]">
			  Let's have a <br />Conversation
			</h1>
			<p class="mt-4 w-full text-lg font-light leading-7 text-white">
			  Tell us how we can help, and a member of <br />our team will be in touch soon.
			</p>
		</div>
		<!-- User Input Form -->
	<div class="absolute p-6 w-full md:w-[50%] mx-auto md:mx-0 md:ml-auto  md:right-0 md:top-[45%] md:transform md:translate-y-[-50%]">
		<form
			id="contactForm"
			on:submit={handleSubmit}
			class="flex flex-col justify-center p-5 text-base font-light bg-white rounded-2xl border border-solid shadow-lg border-black border-opacity-10 max-w-[560px]"
		>
			<label for="fullName" class="sr-only">Full Name</label>
			<input
				type="text"
				id="fullName"
				bind:value={fullName}
				placeholder="Full Name"
				required
				class="px-4 py-3 bg-white rounded-md border border-solid border-black border-opacity-10 leading-[160%] text-neutral-400 max-md:pr-5 max-md:max-w-full"
			/>

			<label for="email" class="sr-only">Email Address</label>
			<input
				type="email"
				id="email"
				bind:value={email}
				placeholder="Email Address"
				required
				class="px-4 py-3 mt-5 bg-white rounded-md border border-solid border-black border-opacity-10 leading-[160%] text-neutral-400 max-md:pr-5 max-md:max-w-full"
			/>

			<div class="flex gap-3 mt-5 whitespace-nowrap bg-white rounded-md border border-solid border-black border-opacity-10 leading-[160%] max-md:flex-wrap">
				<CountryCodeSelector />
				<label for="phoneNumber" class="sr-only">Phone Number</label>
				<input
					type="tel"
					id="phoneNumber"
					bind:value={phoneNumber}
					placeholder="000-000-0000"
					class="my-auto text-neutral-400 flex-grow"
				/>
			</div>

			<label for="message" class="sr-only">Message</label>
			<textarea
				id="message"
				bind:value={message}
				placeholder="Message"
				required
				class="px-4 pt-3 pb-8 mt-5 whitespace-nowrap bg-white rounded-md border border-solid border-black border-opacity-10 leading-[160%] text-neutral-400 max-md:pr-5 max-md:max-w-full"
			></textarea>

			<div class="flex gap-2 mt-5 text-xs leading-5 text-emerald-500 max-md:flex-wrap">
				<input
					type="checkbox"
					id="agreePolicy"
					bind:checked={agreedToPolicy}
					class="form-checkbox"
				/>
				<label for="agreePolicy" class="flex items-center cursor-pointer">
					<span class="underline max-md:max-w-full">
						I have read and agreed to Dhara <a href="/privacy-policy" class="text-emerald-500 underline">Privacy Policy</a> and agree to receive communications
					</span>
				</label>
			</div>

			<button
				type="submit"
				class="px-2.5 py-3 mt-10 text-white whitespace-nowrap bg-emerald-500 rounded-md max-md:px-5 max-md:max-w-full"
			>
				Submit
			</button>
		</form>
	</div>
	<!-- End User Input Form -->
		<Convo />
	</div>
</section>
