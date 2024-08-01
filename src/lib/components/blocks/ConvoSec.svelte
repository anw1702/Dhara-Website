<script lang="ts">
	import Convo from '@/img/convo.svelte';
	import CountryCodeSelector from './CountryCodeSelector.svelte';
	import ConvoMobile from '@/img/ConvoMobile.svelte';

	let fullName = '';
	let email = '';
	let message = '';
	let agreedToPolicy = false;
</script>

<!-- Convo section -->
<section class="relative mx-auto mb-56 flex items-center justify-center">
	<div
		class="absolute mx-auto hidden w-full p-6 text-white dark:text-gray-200 md:left-[10%] md:top-[45%] md:mx-0 md:mr-auto md:w-[50%] md:translate-y-[-40%] md:transform lg:block"
	>
		<h1 class="w-full text-5xl font-medium leading-[58px] dark:text-white">
			Let's have a <br />Conversation
		</h1>
		<p class="mt-4 w-full text-lg font-light leading-7 dark:text-white">
			Tell us how we can help, and a member of <br />our team will be in touch soon.
		</p>
	</div>
	<!-- User Input Form -->
	<div
		class="absolute mx-auto w-full p-6 md:right-0 md:top-[45%] md:mx-0 md:ml-auto md:w-[50%] md:translate-y-[-50%] md:transform"
	>
		<form
			id="contactForm"
			class="flex max-w-[560px] flex-col justify-center rounded-2xl border border-solid border-black border-opacity-10 bg-white p-5 text-base font-light shadow-lg dark:border-gray-700 dark:bg-gray-900"
		>
			<label for="fullName" class="sr-only">Full Name</label>
			<input
				type="text"
				id="fullName"
				bind:value={fullName}
				placeholder="Full Name"
				required
				class="rounded-md border border-solid border-black border-opacity-10 bg-white px-4 py-3 leading-[160%] text-neutral-400 dark:border-gray-700 dark:bg-gray-200 max-md:max-w-full max-md:pr-5"
			/>

			<label for="email" class="sr-only">Email Address</label>
			<input
				type="email"
				id="email"
				bind:value={email}
				placeholder="Email Address"
				required
				class="mt-5 rounded-md border border-solid border-black border-opacity-10 bg-white px-4 py-3 leading-[160%] text-neutral-400 dark:border-gray-700 dark:bg-gray-200 max-md:max-w-full max-md:pr-5"
			/>

			<div
				class="mt-5 flex gap-3 whitespace-nowrap rounded-md border border-solid border-black border-opacity-10 bg-white leading-[160%] dark:border-gray-700 dark:bg-gray-700 max-md:flex-wrap"
			>
				<CountryCodeSelector />
			</div>

			<label for="message" class="sr-only">Message</label>
			<textarea
				id="message"
				bind:value={message}
				placeholder="Message"
				required
				class="mt-5 whitespace-nowrap rounded-md border border-solid border-black border-opacity-10 bg-white px-4 pb-8 pt-3 leading-[160%] text-neutral-400 dark:border-gray-700 dark:bg-gray-200 max-md:max-w-full max-md:pr-5"
			></textarea>

			<div
				class="mt-5 flex gap-2 text-xs leading-5 text-emerald-500 dark:text-gray-400 max-md:flex-wrap"
			>
				<input
					type="checkbox"
					id="agreePolicy"
					bind:checked={agreedToPolicy}
					class="form-checkbox"
				/>
				<label for="agreePolicy" class="flex cursor-pointer items-center">
					<span class="underline max-md:max-w-full">
						I have read and agreed to Dhara <a
							href="/privacy-policy"
							class="text-emerald-500 underline">Privacy Policy</a
						> and agree to receive communications
					</span>
				</label>
			</div>

			<button
				type="submit"
				class="mt-10 whitespace-nowrap rounded-md bg-emerald-500 px-2.5 py-3 text-white dark:bg-emerald-500 dark:text-white max-md:max-w-full max-md:px-5"
			>
				Submit
			</button>
		</form>
	</div>
	<!-- End User Input Form -->
	<!-- Text Area -->
	<!-- End of Text Area -->
	<div class="hidden dark:text-gray-300 lg:block">
		<Convo />
	</div>
	<div class="relative right-3 top-52 -z-10 w-[90vw] dark:text-gray-300 lg:hidden">
		<ConvoMobile size="fit" />
	</div>
	<!-- Mobile text -->
	<span
		class="absolute -bottom-40 max-w-screen-lg space-y-3 text-white dark:text-gray-400 lg:hidden"
	>
		<h4 class="text-3xl dark:text-gray-300 md:text-4xl">Let’s have a Conversation</h4>
		<h6 class="max-w-sm text-wrap text-base dark:text-gray-300">
			Tell us how we can help, and a member of our team will be in touch soon.
		</h6>
	</span>
	<!-- End of Mobile text -->
</section>
<!-- End of Convo section -->
