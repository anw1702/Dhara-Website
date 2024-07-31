<script lang="ts">
	import Inner from './IconWrapper/Inner.svelte';
	import Building from '@/img/building.svelte';
	import TruckKun from '@/img/truck-kun.svelte';
	import IconWrapper from '@/components/blocks/IconWrapper/IconWrapper.svelte';
	import leftGif from '@/img/b3151c0a6afdefc2137c73255408a557-ezgif.com-crop.gif';
	import rightGif from '@/img/111abeed6207fb60b16fc333a023d217-ezgif.com-crop.gif';
	import MobileRight from '@/img/mobile-right.svelte';
	import MobileLeft from '@/img/mobile-left.svelte';
	import Cart from '@/img/cart.svelte';
	import Shop from '@/img/shop.svelte';
	import { Play } from 'lucide-svelte';
	import PhoneSmall from '@/img/Phone-Section-Mobile.svelte';
	import PhoneBig from '@/img/Phone-Section-Desktop.svelte';
</script>

<section class="relative mx-auto px-4 py-8">
	<div class="flex justify-between">
		<IconWrapper class="lg:hidden">
			<Inner>
				<Cart />
			</Inner>
		</IconWrapper>

		<h1
			class="mx-auto mb-4 mt-5 text-center text-2xl font-bold text-dharateal dark:text-white md:text-3xl lg:mt-8 lg:text-6xl lg:text-gray-400"
		>
			Deep Financing Tokens
		</h1>
		<IconWrapper class="lg:hidden">
			<Inner>
				<Shop />
			</Inner>
		</IconWrapper>
	</div>

	<div class="mb-4">
		<p
			class="mx-auto mb-4 text-center text-2xl text-dharateal dark:text-gray-300 md:text-3xl lg:mt-8 lg:text-6xl lg:text-gray-400"
		>
			A Fintech Innovation
		</p>
	</div>

	<div class="relative flex justify-center">
		<div class="relative w-1/2">
			<img src={leftGif} alt="GIF 1" class="hidden w-full lg:mt-16 lg:block" />
		</div>
		<div class="absolute left-0 h-fit lg:hidden">
			<MobileLeft />
		</div>
		<div class="xl:mt-[3.4vw]">
			<p class="max-w-auto text-center text-sm font-normal text-stone-500 lg:text-lg">
				Transforming Supply Chain Finance with Programmable Digital Assets. Bridging the Liquidity
				Gap in Global Supply Chains.
			</p>

			<div class="mx-auto mt-8 flex items-center justify-center space-x-3 xs:mt-12 lg:mt-8">
				<button
					class="flex w-fit items-center rounded-lg bg-dharateal p-2 text-center text-xs font-medium text-white hover:bg-dharateal focus:outline-none focus:ring-4 focus:ring-dharateal dark:hover:bg-gray-600 dark:focus:ring-gray-500 lg:p-3 lg:text-base"
				>
					Book a Demo
				</button>

				<button
					class="mx-3 flex items-center justify-center space-x-2 rounded-lg bg-transparent px-4 py-2"
				>
					How it works
					<span class="ml-2 rounded-full bg-dharateal p-1">
						<Play class="fill-white" strokeWidth={1} size={12} absoluteStrokeWidth={true} />
					</span>
				</button>
			</div>
		</div>

		<div class="absolute right-0 h-fit lg:hidden">
			<MobileRight />
		</div>
		<div class="relative w-1/2">
			<img src={rightGif} alt="GIF 2" class="hidden w-full lg:mt-16 lg:block" />
		</div>
	</div>
	<!-- Phone Section -->
	<div class="relative mx-auto my-5 flex flex-col justify-center space-y-5 lg:my-16">
		<span class="mx-auto lg:hidden">
			<PhoneSmall />
		</span>
		<!-- Desktop View -->
		<div class="relative mx-auto hidden w-fit lg:block">
			<div class="relative">
				<PhoneBig />
				<!-- Added Icons for Desktop View -->
				<div class="absolute left-0 top-0 ml-[-80px] mt-[-50px] hidden lg:block">
					<IconWrapper class="size-14">
						<Inner class="size-10">
							<Cart />
						</Inner>
					</IconWrapper>
				</div>
				<div class="absolute right-0 top-0 mr-[-80px] mt-[-50px] hidden xl:block">
					<IconWrapper class="size-14">
						<Inner class="size-10">
							<Shop />
						</Inner>
					</IconWrapper>
				</div>
				<div class="left-05 absolute bottom-0 mb-[-50px] ml-[-80px] hidden lg:block">
					<IconWrapper class="size-14">
						<Inner class="size-10">
							<Building />
						</Inner>
					</IconWrapper>
				</div>
				<div class="absolute bottom-36 right-0 mb-[-50px] mr-[-80px] hidden xl:block">
					<IconWrapper class="size-14">
						<Inner class="size-10">
							<TruckKun />
						</Inner>
					</IconWrapper>
				</div>
			</div>
		</div>
		<!-- End of Desktop View -->
		<!-- Mobile view -->
		<div class="flex justify-between px-12">
			<IconWrapper class="lg:hidden">
				<Inner>
					<Building />
				</Inner>
			</IconWrapper>
			<IconWrapper class="lg:hidden">
				<Inner>
					<TruckKun />
				</Inner>
			</IconWrapper>
		</div>
		<!-- End of Mobile view -->
	</div>
</section>
