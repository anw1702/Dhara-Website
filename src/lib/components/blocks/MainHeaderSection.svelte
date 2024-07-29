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
			class="mx-auto mb-4 mt-5 text-center text-2xl font-bold text-black md:text-3xl lg:mt-8 lg:text-6xl lg:text-gray-500"
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
			class="mx-auto mb-4 text-center text-2xl text-dharateal md:text-3xl lg:mt-8 lg:text-6xl lg:text-gray-500"
		>
			A Fintech Innovation
		</p>
	</div>

	<div class="flex justify-center">
		<div class="mr-4 w-1/2">
			<img src={leftGif} alt="GIF 1" class="relative hidden w-full lg:mt-16 lg:block" />
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
					class="flex w-fit items-center rounded-lg bg-dharateal p-2 text-center text-xs font-medium text-white hover:bg-dharateal focus:outline-none focus:ring-4 focus:ring-dharateal dark:bg-dharateal dark:hover:bg-dharateal dark:focus:ring-dharateal lg:p-3 lg:text-base"
				>
					Book a Demo
				</button>

				<button
					class="mx-3 flex items-center justify-center space-x-2 rounded-lg bg-white px-4 py-2"
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
		<div class="ml-4 w-1/2">
			<img src={rightGif} alt="GIF 2" class="relative hidden w-full lg:mt-16 lg:block" />
		</div>
	</div>
	<!-- Phone Section -->
	<div class="mx-auto my-2 flex flex-col justify-center space-y-5 lg:my-16">
		<span class="mx-auto lg:hidden">
			<PhoneSmall />
		</span>
		<!-- Desktop View -->
		<div>
			<div class="mb-10 flex justify-between">
				<IconWrapper class="hidden p-3 lg:block">
					<Inner class="size-12">
						<Cart width="fit" height="fit" />
					</Inner>
				</IconWrapper>
				<IconWrapper class="hidden p-3 lg:block">
					<Inner class="size-12">
						<Shop width="fit" height="fit" />
					</Inner>
				</IconWrapper>
			</div>
			<div class="mx-auto hidden w-fit lg:block">
				<PhoneBig />
			</div>
			<div class="relative mt-10 flex justify-between">
				<IconWrapper class="hidden p-3 lg:block">
					<Inner class="size-12">
						<Building width="fit" height="fit" />
					</Inner>
				</IconWrapper>
				<span class="bottom-80 xl:absolute xl:right-16">
					<IconWrapper class="hidden p-3 lg:block">
						<Inner class="size-12">
							<TruckKun width="fit" height="fit" />
						</Inner>
					</IconWrapper>
				</span>
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
