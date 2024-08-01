<script>
	import { navItems } from '@/index';
	import { ArrowUpRight } from 'lucide-svelte';
	import Twitter from '@/img/twitter.svelte';
	import { Link } from 'svelte-routing';
	import Linkedin from '@/img/linkedin.svelte';
	import Instagram from '@/img/instagram.svelte';
	const links = ['Terms of Use', 'Privacy Policy', 'Contact Us'];
</script>

<footer
	class="font-lexend border-t-solid border-t border-gray-200 bg-white py-10 dark:border-gray-800 dark:bg-gray-800 dark:text-white"
>
	<div class="container grid grid-cols-2 gap-1 dark:border-gray-700 md:grid-cols-3">
		<div class="text-left dark:text-gray-300">
			<div class="flex flex-col items-start">
				<p class="mb-4 text-base md:text-xl">
					Transform your Supply Chain Finance with Programmable Digital Assets.
				</p>
				<button
					class="hover:bg-[#048C6F flex w-fit items-center rounded bg-dharateal px-4 py-2 dark:bg-gray-700 dark:hover:bg-gray-600"
				>
					Request Demo
					<ArrowUpRight class="ml-2" />
				</button>
			</div>
		</div>
		<div class="text-center dark:text-gray-300">
			<h2 class="mb-4 mr-5 text-lg">DHARA</h2>
			<nav class="mx-auto flex w-fit flex-col space-y-2 text-left dark:text-gray-400">
				{#each navItems as item}
					<a
						href={item.toLowerCase().split(' ').join('-')}
						class="hover:text-dharateal dark:hover:text-gray-300">{item}</a
					>
				{/each}
			</nav>
		</div>
		<div class="col-span-2 text-left dark:text-gray-300 md:col-span-1 md:block md:text-right">
			<p class="mb-4 text-xl md:text-left">
				Stay updated with the latest updates on deep finance tokenization.
			</p>
			<div class="flex justify-center md:justify-end">
				<div
					class="flex w-full overflow-hidden rounded border border-gray-300 focus-within:ring-2 focus-within:ring-dharateal dark:border-gray-600"
				>
					<input
						type="email"
						placeholder="Email address"
						class="flex-1 px-2 py-4 focus:outline-none dark:bg-gray-700"
					/>
					<button
						class="mb-2 mr-1 mt-2 rounded bg-dharateal px-2 py-2 hover:bg-[#048C6F] dark:bg-dharateal dark:text-black dark:hover:bg-[#048c6fd4]"
						>Subscribe</button
					>
				</div>
			</div>
		</div>
	</div>

	<div
		class="container mx-auto mt-10 flex flex-col items-center dark:text-gray-400 md:flex-row md:justify-between"
	>
		<div class="mb-4 flex flex-col md:mb-0">
			<p class="text-sm font-medium">Follow us on social media:</p>
			<div class="mt-2 flex items-center space-x-4">
				<!-- Social Media Icons -->
				<a href="/TwitterRoute" class="hover:text-dharateal dark:hover:text-gray-300">
					<Twitter />
				</a>
				<a href="/LinkedInRoute" class="hover:text-dharateal dark:hover:text-gray-300">
					<Linkedin />
				</a>
				<a href="/InstaRoute" class="hover:text-dharateal dark:hover:text-gray-300">
					<Instagram />
				</a>
			</div>
		</div>
		<nav class="flex space-x-4">
			<a href="/terms" class="hover:text-dharateal dark:hover:text-gray-300">Terms of Use</a>
			<a href="/privacy" class="hover:text-dharateal dark:hover:text-gray-300">Privacy Policy</a>
			<a href="/contact-us" class="hover:text-dharateal dark:hover:text-gray-300">Contact Us</a>
		</nav>
	</div>
</footer>
