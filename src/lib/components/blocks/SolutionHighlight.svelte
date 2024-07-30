<script lang="ts">
	import Inner from '@/components/blocks/IconWrapper/Inner.svelte';
	import IconWrapper from '@/components/blocks/IconWrapper/IconWrapper.svelte';
	import TruckKun from '@/img/truck-kun.svelte';
	import Cart from '@/img/cart.svelte';
	import Shop from '@/img/shop.svelte';
	import Building from '@/img/building.svelte';
	import { ArrowUpRight } from 'lucide-svelte';
	import UnlockLeft from '@/img/UnlockLeft.svelte';
	import UnlockRight from '@/img/UnlockRight.svelte';
	import UnlockRightMobile from '@/img/UnlockRightMobile.svelte';
	import UnlockLeftMobile from '@/img/UnlockLeftMobile.svelte';
</script>

<div
	class="relative -z-20 mx-auto mb-12 mt-12 flex h-[40vh] w-[70vw] flex-col overflow-hidden rounded-xl bg-gradient-to-l from-[#05A987] to-[#024336] text-center"
>
	<span class="absolute left-0 -z-10 hidden lg:block">
		<UnlockRight />
	</span>
	<span class="absolute left-0 -z-10 lg:hidden">
		<UnlockLeftMobile />
	</span>
	<!-- Added Icons inside the main box -->
	<span class="flex">
		<div class="left-0 top-0 ml-3 mt-[50px] md:ml-[50px] lg:absolute">
			<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px] dark:bg-gray-600">
				<Inner class="size-7 rounded-[5px] bg-[#05A987] md:size-10">
					<Building width="fit" height="fit" stroke="white" />
				</Inner>
			</IconWrapper>
		</div>
		<h3
			class="mx-auto mt-24 text-xl text-white dark:text-gray-200 md:text-3xl lg:mt-16 lg:text-4xl"
		>
			Unlock the Power of Our Solutions,
		</h3>
		<div class="right-0 top-0 mr-3 mt-[50px] md:mr-[50px] lg:absolute">
			<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px] dark:bg-gray-600">
				<Inner class="size-7 rounded-[5px] bg-[#05A987] md:size-10">
					<TruckKun width="fit" height="fit" stroke="white" />
				</Inner>
			</IconWrapper>
		</div>
	</span>

	<h3 class="mx-auto text-xl text-white dark:text-gray-200 md:text-3xl lg:text-4xl">
		Get FREE expert guidance.
	</h3>
	<button
		class="mx-auto mt-10 flex w-fit justify-between rounded-md bg-white p-3 text-sm dark:bg-gray-900 md:text-base"
	>
		Request Demo <ArrowUpRight />
	</button>

	<span class="mt-5 flex justify-center lg:mt-10">
		<div class="bottom-0 left-0 mb-[50px] ml-[200px] lg:absolute">
			<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px] dark:bg-gray-600">
				<Inner class="size-7 rounded-[5px] bg-[#05A987] md:size-10">
					<Shop width="fit" height="fit" stroke="white" />
				</Inner>
			</IconWrapper>
		</div>
		<!-- fix for spacing -->
		<div class="mx-auto min-w-[30vw]"></div>
		<!-- fix for spacing -->
		<div class="bottom-0 right-0 mb-[50px] mr-[200px] lg:absolute">
			<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px] dark:bg-gray-600">
				<Inner class="size-7 rounded-[5px] bg-[#05A987] md:size-10">
					<Cart width="fit" height="fit" stroke="white" />
				</Inner>
			</IconWrapper>
		</div>
	</span>

	<span class="absolute right-0 -z-10 hidden lg:block">
		<UnlockLeft />
	</span>
	<span class="absolute right-0 -z-10 lg:hidden">
		<UnlockRightMobile />
	</span>
</div>
