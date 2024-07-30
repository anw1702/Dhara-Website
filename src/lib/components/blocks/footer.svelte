<script>
	import { navItems } from '@/index';
	import { ArrowUpRight } from 'lucide-svelte';
	import Twitter from '@/img/twitter.svelte';
	import { Link } from 'svelte-routing';
	import Linkedin from '@/img/linkedin.svelte';
	import Instagram from '@/img/instagram.svelte';
	const links = ['Terms of Use', 'Privacy Policy', 'Contact Us'];
</script>

<footer class="font-lexend border-t-solid border-t border-gray-200 bg-white py-10">
	<div class="container grid grid-cols-2 gap-1 md:grid-cols-3">
		<div class="text-left">
			<div class="flex flex-col items-start">
				<p class="mb-4 text-base md:text-xl">
					Transform your Supply Chain Finance with Programmable Digital Assets.
				</p>
				<button
					class="flex w-fit items-center rounded bg-dharateal px-4 py-2 text-white hover:bg-[#048C6F]"
				>
					Request Demo
					<ArrowUpRight class="ml-2" />
				</button>
			</div>
		</div>
		<div class="text-center">
			<h2 class="mb-4 mr-5 text-lg">DHARA</h2>
			<nav class="mx-auto flex w-fit flex-col space-y-2 text-left">
				{#each navItems as item}
					<a
						href={item.toLowerCase().split(' ').join('-')}
						class="text-gray-800 hover:text-dharateal">{item}</a
					>
				{/each}
			</nav>
		</div>
		<div class="col-span-2 text-left md:col-span-1 md:block md:text-right">
			<p class="mb-4 text-xl md:text-left">
				Stay updated with the latest updates on deep finance tokenization.
			</p>
			<div class="flex justify-center md:justify-end">
				<div
					class="flex w-full overflow-hidden rounded border border-gray-300 focus-within:ring-2 focus-within:ring-dharateal"
				>
					<input
						type="email"
						placeholder="Email address"
						class="flex-1 px-2 py-4 focus:outline-none"
					/>
					<button
						class="mb-2 mr-1 mt-2 rounded bg-dharateal px-2 py-2 text-white hover:bg-[#048C6F]"
						>Subscribe</button
					>
				</div>
			</div>
		</div>
	</div>

	<div class="container mx-auto mt-10 flex flex-col items-center md:flex-row md:justify-between">
		<div class="flex flex-col mb-4 md:mb-0">
			<p class="text-sm font-medium">Follow us on social media:</p>
			<div class="mt-2 flex items-center space-x-4">
				<!-- Social Media Icons -->
				<a href="/TwitterRoute" class="hover:text-dharateal text-gray-600">
					<Twitter />
				</a>
				<a href="/LinkedInRoute" class="hover:text-dharateal text-gray-600">
					<Linkedin />
				</a>
				<a href="/InstaRoute" class="hover:text-dharateal text-gray-600">
					<Instagram />
				</a>
			</div>
		</div>
		<nav class="flex space-x-4">
			<a href= "/terms" class="hover:text-dharateal text-gray-800">Terms of Use</a>
			<a href="/privacy" class="hover:text-dharateal text-gray-800">Privacy Policy</a>
			<a href="/contact-us" class="hover:text-dharateal text-gray-800">Contact Us</a>
		</nav>
	</div>
</footer>
